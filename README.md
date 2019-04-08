![](https://image-static.segmentfault.com/384/292/3842924659-5ca8af767bf9c_articlex)

# Awesome Sparklyr

![](https://camo.githubusercontent.com/1997c7e760b163a61aba3a2c98f21be8c524be29/68747470733a2f2f617765736f6d652e72652f62616467652e737667)

## Goal

Sparklyr is pretty awesome tool for parallel programming.

This repo aims for collecting awesome Sparklyr resources togather.

## How to Contribute

1. fork this project.
2. Add your resources by pull request.

## Community

+ [RStudio Forum](https://community.rstudio.com/)
+ [![](https://camo.githubusercontent.com/62773cf061398aeb23950eb3e440115a687d67d2/68747470733a2f2f6261646765732e6769747465722e696d2f7273747564696f2f737061726b6c79722e737667)](https://gitter.im/rstudio/sparklyr?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

## Sparklyr Family

+ [rsparkling: Use H2O Sparkling Water from R (Spark + R + Machine Learning)](https://github.com/h2oai/sparkling-water/tree/master/r)

## Sparklyr Cheatsheet

+ [en: Data Science in Spark with Sparklyr::CHEAT SHEET](https://ugoproto.github.io/ugo_r_doc/sparklyr.pdf)
+ [zh: Spark数据科学之 sparklyr 速查表](https://github.com/rstudio/cheatsheets/raw/master/translations/chinese/sparklyr-cheatsheet_zh_CN.pdf)
+ [de: Data Science in Spark mit sparklyr Schummelzettel](https://github.com/rstudio/cheatsheets/raw/master/translations/german/sparklyr-cheatsheet_de.pdf)


## Sparklyr Related Database

### Sparklyr Tidy

+ [sparklyr.nested: A sparklyr extension for nested data](https://github.com/mitre/sparklyr.nested) ![](https://camo.githubusercontent.com/bee62001eaf4c58d69c524724204929a9190ba9a/687474703a2f2f6372616e6c6f67732e722d706b672e6f72672f6261646765732f6772616e642d746f74616c2f737061726b6c79722e6e6573746564)

### Sparklyr Storage Engine

> avro vs parquet: row-oriented vs column-oriented, see more introduction in [stackoverflow](https://stackoverflow.com/questions/28957291/avro-vs-parquet) and [cern blog](https://db-blog.web.cern.ch/blog/zbigniew-baranowski/2017-01-performance-comparison-different-file-formats-and-storage-engines)
+ [sparkavro: Load Avro data into Spark with sparklyr](https://github.com/chezou/sparkavro) 


### Sparklyr Streaming

### Sparklyr Tikv

+ [TiSparkR: R interface for TiSpark](https://github.com/pingcap/tispark/tree/master/R)

### Redshift

+ [sparkredshift: An R package to read data from Amazon Redshift into Spark DataFrames](https://github.com/Emaasit/sparkredshift)

### Big Query

+ [sparkbq: Sparklyr extension package to connect to Google BigQuery](https://github.com/miraisolutions/sparkbq)

### Pivotal

+ [PivotalR: An convenient R tool for manipulating tables in PostgreSQL type databases and a wrapper of Apache MADlib](https://github.com/pivotalsoftware/PivotalR)

### Impala

+ [implyr: SQL backend to dplyr for Impala](https://github.com/ianmcook/implyr)

### Presto

+ [RPresto: DBI-based adapter for Presto for the statistical programming language R](https://github.com/prestodb/RPresto)


## Sparklyr Algorithm

### Machine Learning Production Pipeline

+ [mleap: R Interface to MLeap](https://github.com/rstudio/mleap)
+ [mlflow: R interface for MLflow](https://github.com/mlflow/mlflow/tree/master/mlflow/R/mlflow)

### Geospatial Data

+ [geospark: bring sf to spark in production](https://github.com/harryprince/geospark)
+ [sparkgeo: Sparklyr extension package providing geospatial analytics capabilities](https://github.com/miraisolutions/sparkgeo)

### Text Mining

+ [spacyr-sparklyr: Example code of spacyr with sparklyr](https://github.com/chezou/spacyr-sparklyr)

### Graph Mining

+ [graphframes: R Interface for GraphFrames](https://github.com/rstudio/graphframes)

### Time Series 

+ [sparkts: sparklyr interface to the spark-ts package](https://github.com/nathaneastwood/sparkts)

### Deep Learning

+ [sparktf: R interface to Spark TensorFlow Connector](https://github.com/rstudio/sparktf)

### Tree Model

+ [sparkxgb: R interface for XGBoost on Spark](https://github.com/rstudio/sparkxgb)

## Spakrlyr Administration

+ [cloudera-parcel: customized cloudera-parcel](https://github.com/chezou/cloudera-parcel)
+ [mvndeps: Use (previously installed) maven from R to resolve java dependencies](https://github.com/mitre/mvndeps)
+ [clusterconf: Manage Hadoop cluster configurations](https://github.com/mitre/clusterconf)

## Sparklyr Courses

+ [DataCamp: Introduction to Spark in R using sparklyr](https://www.datacamp.com/courses/introduction-to-spark-in-r-using-sparklyr)

+ [RStudio Webinars: Part 1 - Introducing an R interface for Apache Spark](https://resources.rstudio.com/webinars/introducing-an-r-interface-for-apache-spark)
+ [RStudio Webinars: Part 2 - Extending Spark using sparklyr](https://resources.rstudio.com/webinars/extending-spark-using-sparklyr)
+ [RStudio Webinars: Part 3 - Advanced features of sparklyr](https://resources.rstudio.com/webinars/advanced-features-of-sparklyr)
+ [RStudio Webinars: Part 4 - Understanding sparklyr deployment modes](https://resources.rstudio.com/webinars/understanding-sparklyr-deployment-modes)

## Sparklyr Blogs

### RStudio Official Blog

+ [sparklyr 1.0: Apache Arrow, XGBoost, Broom and TFRecords](https://blog.rstudio.com/2019/03/15/sparklyr-1-0/)
+ [sparklyr 0.9: Streams and Kubernetes](https://blog.rstudio.com/2018/10/01/sparklyr-0-9/)
+ [sparklyr 0.8: Production pipelines and graphs](https://blog.rstudio.com/2018/05/14/sparklyr-0-8/)
+ [sparklyr 0.7: Spark Pipelines and Machine Learning](https://blog.rstudio.com/2018/01/29/sparklyr-0-7/)
+ [sparklyr 0.6: Distributed R and external sources](https://blog.rstudio.com/2017/07/31/sparklyr-0-6/)
+ [sparklyr 0.5: Livy and dplyr improvements](https://blog.rstudio.com/2017/01/24/sparklyr-0-5/)

### Administration

+ [How-to: Automate Your sparklyr Environment with Cloudera Director](https://blog.cloudera.com/blog/2016/12/automating-your-sparklyr-environment-with-cloudera-director/?_ga=1.264069893.826902665.1483652158)

### Comparison

+ [深入对比数据科学工具箱: SparkR vs Sparklyr](https://cosx.org/2018/05/sparkr-vs-sparklyr)

### Best Practice Example

+ [Online retail data analysis using R, tidyverse, sparklyr and Spark](https://rstudio-pubs-static.s3.amazonaws.com/430563_d38c12b53d724fa6852949b1f3e4ffbf.html)
+ [Spark Joy - Saying Konmari to your event logs with grammar of data manipulation](https://etheleon.github.io/articles/spark-joy/)
+ [How to Distribute your R code with sparklyr and Cloudera Data Science Workbench](https://blog.cloudera.com/blog/2017/09/how-to-distribute-your-r-code-with-sparklyr-and-cdsw/)
+ [Association rules using FPGrowth in Spark MLlib through SparklyR](https://longhowlam.wordpress.com/2017/11/23/association-rules-using-fpgrowth-in-spark-mllib-through-sparklyr/)
+ [Visualizing taxi trips between NYC neighborhoods with Spark and Microsoft R Server](https://blog.revolutionanalytics.com/2016/12/taxi-mrs-spark.html)

### Introduction

+ [Microsoft RxSpark: Create Spark compute context, connect and disconnect a Spark application](https://docs.microsoft.com/en-us/machine-learning-server/r-reference/revoscaler/rxspark)
+ [sparklyr RStudio 활용](https://statkclee.github.io/bigdata/ds-sparklyr.html)
+ [S3のデータをRStudioとsparklyrで分析する](https://blog.cloudera.co.jp/rspark-with-cloudera-director-ee9ac5826f19)
+ [RStudio + sparklyr on EMRでスケーラブル機械学習](http://smrmkt.hatenablog.jp/entry/2017/01/25/205608)
+ [RSparkling: The Best of R + H2O + Spark](https://dzone.com/articles/rsparkling-gt-the-best-of-r-h2o-spark)

## Sparklyr Slides or Talks

+ [Spark+R 大数据分析入门](https://github.com/lix90/Rnotes/raw/master/Spark%2BR_bigdata_intro.pdf)
+ [rstudio-conf-2018-sparklyr](https://s3-us-west-2.amazonaws.com/kevinykuo/rsconf-sparklyr/rstudio-conf-2018-sparklyr.html)
+ [SPARK+AI SUMMIT 2018: From Prototyping to Deployment at Scale with R and sparklyr Kevin Kuo (RStudio)](https://vimeo.com/274395988)
+ [rstudio: building-spark-ml-pipelines-with-sparklyr](https://www.rstudio.com/resources/videos/building-spark-ml-pipelines-with-sparklyr/)
+ [oreilly: Sparklyr: An R interface for Apache Spark](https://cdn.oreillystatic.com/en/assets/1/event/193/Sparklyr_%20An%20R%20interface%20for%20Apache%20Spark%20Presentation.pdf)
+ [DataScienceWarsaw25: sparklyr: R interface to Apache Spark machine learning algorithms with dplyr back-end](http://r-addict.com/DataScienceWarsaw25/show/#/)
+ [Tensorflow and Sparklyr: Scaling Deep Learning and R to the Big Data ecosystem [Italian]](https://www.youtube.com/watch?v=VnaCn9qr0PU)
+ [Sparklyr: Big Data enabler for R users - Serena Signorelli, ICTEAM](https://www.slideshare.net/ds_mi/sparklyr-big-data-enabler-for-r-users-serena-signorelli-icteam)
+ [eRum 2018: Exploiting Spark for high-performance scalable data engineering and data-science on Microsoft Azure ](https://fieldy6961public.blob.core.windows.net/erum2018/erum2018whichSpark.pdf)
