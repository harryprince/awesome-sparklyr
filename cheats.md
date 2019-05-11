
* get **first/last** value over a group

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
