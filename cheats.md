
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

https://github.com/rstudio/sparklyr/issues/1051

* get **datediff**

```
mutate(diff = datediff(end, start) 
```

https://github.com/rstudio/sparklyr/issues/231

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
