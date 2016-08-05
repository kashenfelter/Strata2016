# Strata2016
Materials for Nathan and Garrett's tutorial R for Big Data

# R for big data

## Slides to repurpose: https://www.dropbox.com/sh/thz33i0zfgfnm9w/AAB4l1NcaKFqkOD2gj36eDNya?dl=0

## Key concepts

### Scope: Big data

* R is an excellent big data solution
* Connecting to relational databases
* Working with data at scale in spark
* Using dplyr for data hygiene/tidy (big data best practices)
  * spark, rdbms, R
* Toolchain: Data > model building > sharing
* Introduce notebooks: Do everything in notebooks

## Intro to R and dplyr (slides: Garrett)

> No matter how complex and polished the individual operations are, it is often the quality of the glue that most directly determines the power of the system. — Hal Abelson.

1. R
    a.  R is both tools and a glue, and it is a very good glue.
        i.  Preview of R's tools
        ii.  Role of R as an interface between languages
        iii.  Preview of the RStudio tool chain (_details in proportion to the lack of context here_)
2. tidyverse
    a.  Introduction to the R package system
    b.  Like many mature languages, R contains legacy tools that you should avoid. Some of these tools were not designed for big data. 
    c.  The tidyverse encapsulates the most modern tools that work best with big data. The tidyverse is R + organization + best practices.
        i.  The tidyverse is all open source and free
3. dplyr
    a.  dplyr an R package
    b. not only is dplyr the main tool in the tidyverse, dplyr is the glue between R and big data
    c.  have students open an R Markdown document, demonstrate notebook interface and exporting results as nb.html. 
    d.  Teach 
        i.  `select()`
        ii.  `filter()`
        iii.  `mutate()` 
        iv.  `summarise()`
        v.  `left_join()`
        vi.  `right_join()`
        vii.  `inner_join()`
        viii.  `full_join()`
        ix.  `%>%`
    c.  Segue exercise to big data?
    d.  Also dissect modeling code and ggplot code?


## Big data (slides: Garrett)

1. R and Big data
    a.  R copies data into RAM, which has advantages, but it also creates a fundamental limit on the size of data that you can evaluate in R
        i.  But keep in mind, you can put a lot of RAM on a machine (1 TB)
    b. What do you do when you have more data than can fit into RAM? Keep it outside of RAM. Today we will look at two options. There are other ways as well. 
        i.  RDBMS
        ii.  Spark (compare)
        
## SQLite exercise (nycflights13) (slides: Nathan?)

1. What is relational database?
    i. tabular data with indexes
    ii. can be multinodal
    iii. Invented 50 years ago
2. Introduce the flights data set 
    i. The SQL exercise from 2015
        
## Spark intro

1. What is Spark?
    i.  Analytic engine (not a database!) (like R)
    ii.  Distributed / multi-nodal in memory (like R)
    iii.  You can run SQL and machine learning (like R)
    iv.  Run interactive analyses (like R)
    v.  Handles semi-structured data (like R)
    vi.  Handles streaming data (we're still working on this)
    vii.  Runs two modes (1) cluster (typically hadoop) (2) lol (talk about architecture)
2. Explain technologies
    i.  Hadoop, HDFS, Hive, Spark, (show architecture)
    ii.  then talk about R, Sparklyr, and RStudio Server
3. Sparklyr
    i. dplyr
    ii. Spark SQL
    iii. Spark ML
    iv. What about sparkr? Jeff's slides (from UseR!)
    
## Spark demo (full flights data set)

1. [Spark Demo](https://beta.rstudioconnect.com/content/1409/sparkClusterDemo.html)
1. Provision cluster
2. Connect to data
3. Run Spark SQL
4. Run Spark ML

## Spark exercises (nycflights13 data set)

1. Student exercise (local)

## Communicating

1. Media
    1. Flexdashboard (interactive)
    2. Shiny app
    3. Notebook
    4. Slideshows
    5. R Markdown document / email
2. Platform
    1. RSC

## Conclusion: Toolchain Demo

*from Roger*

[Toolchain images](https://beta.rstudioconnect.com/connect/#/apps/1416)

