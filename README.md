## Spark on Docker
### Requirement
* VM has more than 2GB memory

### Getting Started

* Run and pull docker repository

  `docker run -it -p 8088:8088 -p 8042:8042 -p 4040:4040 -h sandbox bananacoding/spark_hadoop bash`

* Try spark-shell

  `spark-shell`

* Try spark-shell example

  ```
  spark-submit \
  --class org.apache.spark.examples.SparkPi \
  --master yarn \
  --driver-memory 1g \
  --executor-memory 1g \
  --executor-cores 1 \
  $SPARK_HOME/examples/jars/spark-examples*.jar
  ```
* View result in hadoop
  `http://localhost:8088`
