* get **split** value like **strsplit**

```
pattern <- "^(.*)-(.*)$"

df %>% 
   mutate(
     C = regexp_extract(A, pattern, 1),
     D = regexp_extract(A, pattern, 2)
   )
```

```
# Source: spark<?> [?? x 4]
     Id A     C     D    
  <dbl> <chr> <chr> <chr>
1     1 A-B   A     B    
2     2 A-C   A     C    
3     3 A-D   A     D    
```

> https://stackoverflow.com/questions/54522707/sparklyr-split-string-to-string

* get **first/last** value over a group like **dplyr**

```
library(dplyr)
library(sparklyr)

sc <- spark_connect(master = "local",
                    spark_home = "/usr/lib/spark")

thing <- data.frame(values = c(1,1,1,1,2,2,2,2,2,6,6,6,6,10), row_num = 1:14)

thing_tbl <- copy_to(sc, thing)

thing_tbl %>%
  group_by(values) %>%
  summarize(
    first_val = first_value(row_num),
    last_val = last_value(row_num)
  )

```

>https://github.com/rstudio/sparklyr/issues/1051

* get **datediff**

```
mutate(diff = datediff(end, start) 
```

>https://github.com/rstudio/sparklyr/issues/231

* get **pivot table** like **tidyr::spread**

```
thing_tbl <- copy_to(sc, thing  %>% mutate(is_valid = round(runif(14),0)))

 thing_tbl %>% 
    select(row_num, is_valid,cnt) %>% 
  sdf_pivot(formula = row_num ~ is_valid,fun.aggregate = function(gdf) {
  expr <- invoke_static(
          sc,
          "org.apache.spark.sql.functions",
          "expr",
          "sum(values)"
      )

   gdf %>% invoke("agg", expr, list())
 }) %>%
  select(row_num,cnt_invalid = `0.0`,cnt_valid = `1.0`)
  ```
>https://stackoverflow.com/questions/44619000/what-aggregation-functions-can-be-used-with-sdf-pivot-in-sparklyr

* get **word2vec** vocabulary dictionary

```
VECTOR_SIZE = 3

sentence_df <- data.frame(
    sentence = c("Hi I heard about Spark",
                 "I wish Java could use case classes",
                 "Logistic regression models are neat"))
  
sentence_tbl <- sdf_copy_to(sc, sentence_df, overwrite = TRUE)
 
tokenized_tbl <- ft_tokenizer(sentence_tbl, "sentence", "words") %>%
    sdf_register("tokenized")

 model <- ft_word2vec(sc, "words", "result",
                      vector_size= VECTOR_SIZE, min_count = 0) %>%
    ml_fit(tokenized_tbl)
  
 
word_vector_tbl <- model$vectors %>% 
     sparklyr::sdf_separate_column(column = "vector",
                                   into = paste0("f",1:VECTOR_SIZE)) %>% select(-vector)
                                   
word_vector_tbl %>% head()
```
