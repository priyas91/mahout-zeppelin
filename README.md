# mahout-zeppelin

### Setup

Add the following properties to the Spark interpreter in Zeppelin (or create a new interpretter with the following properties added)

```
spark.kryo.registrator  ->	org.apache.mahout.sparkbindings.io.MahoutKryoRegistrator
spark.serializer        ->	org.apache.spark.serializer.KryoSerializer
```

Add the following dependencies to said interpretter: (TODO: change these to maven)
```
artifact	
/home/username/.m2/repository/org/apache/mahout/mahout-math/0.12.1-SNAPSHOT/mahout-math-0.12.1-SNAPSHOT.jar	
/home/username/.m2/repository/org/apache/mahout/mahout-math-scala_2.10/0.12.1-SNAPSHOT/mahout-math-scala_2.10-0.12.1-SNAPSHOT.jar	
/home/username/.m2/repository/org/apache/mahout/mahout-spark_2.10/0.12.1-SNAPSHOT/mahout-spark_2.10-0.12.1-SNAPSHOT.jar	
/home/username/.m2/repository/org/apache/mahout/mahout-spark-shell_2.10/0.12.1-SNAPSHOT/mahout-spark-shell_2.10-0.12.1-SNAPSHOT.jar
/home/username/.m2/repository/org/apache/mahout/mahout-spark-shell_2.10/0.12.1-SNAPSHOT/mahout-spark_2.10-0.12.1-SNAPSHOT-dependency-reduced.jar
```

Run the following (is this nessecary?): 
```
$MAHOUT_HOME/bin/mahout-load-spark-env.sh 
```

Run the following (This is nessecary):
```
export MAHOUT_HOME=[directory into which you checked out Mahout]
export SPARK_HOME=[directory where you unpacked Spark]
export MASTER=[url of the Spark master]
```

Wouldn't hurt to restart Zeppelin...
