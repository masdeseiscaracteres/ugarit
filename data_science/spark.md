# Spark
## Education
### Basic
- [MOOC] [Distributed Computing with Spark SQL by UC Davis](https://www.coursera.org/learn/spark-sql): part of the Learn SQL Basics for Data Science program at Coursera
- [Tutorial] [PySpark Tutorial - Spark by {Examples}](https://sparkbyexamples.com/pyspark-tutorial/)
- [Blog post] [Introducing window functions in Spark SQL](https://databricks.com/blog/2015/07/15/introducing-window-functions-in-spark-sql.html)
- [Blog post] [Best practices for bucketing](https://towardsdatascience.com/best-practices-for-bucketing-in-spark-sql-ea9f23f7dd53)
- [Blog] [David Vrba](https://medium.com/@vrba.dave)

### Advanced
- [Book] [The Internals of Apache Spark](https://books.japila.pl/apache-spark-internals/)
- [Book] [The Internals of Spark SQL](https://jaceklaskowski.github.io/mastering-spark-sql-book/)

## Tools
- [koalas](https://koalas.readthedocs.io/en/latest/index.html): pandas-style wrapper for PySpark

## Documentation
- [Spark API documentation](https://spark.apache.org/docs/latest/): access to all APIs (Java, Scala, Python, R)
  - [Spark Javadocs](https://spark.apache.org/docs/latest/api/java/index.html)
  - [PySpark (Python interface) documentation](https://spark.apache.org/docs/latest/api/python/)
- [Graphframes documentation](http://graphframes.github.io/graphframes/docs/_site/index.html)


## Common issues
- Serialization
  - ["Could not serialize object" error](https://csyhuang.github.io/2019/09/24/pyspark-could-not-serialize-object/)
  - [Cython functions as UDFs](https://github.com/cython/cython/issues/2584)
  - [Using closures to send variables to spark executors](https://stackoverflow.com/questions/52777652/understand-closure-in-spark)
  - [Implement a Java UDF and call it from PySpark](https://stackoverflow.com/questions/36171208/implement-a-java-udf-and-call-it-from-pyspark)
