# 2. PySpark Read File

## Prerequisites

- Complete tutorial #1

## Tutorial

```bash
# Access pyspark in the container
docker exec -it spark-hadoop pyspark

# Setup some variables we'll use for later
inputFormatClass = "org.apache.hadoop.mapreduce.lib.input.TextInputFormat"
keyClass = "org.apache.hadoop.io.LongWritable"
valueClass = "org.apache.hadoop.io.Text"

# Load a file (created in the previous tutorial)
rdd = sc.newAPIHadoopFile("/user/root/test-data/test1.txt", inputFormatClass, keyClass, valueClass)

# View all the contents
rdd.collect()

# View the first line
rdd.first()

# Get the total number of lines
rdd.count()

# Get the first 2 lines
rdd.take(2)
```

## Notes

You will still be in the container, in PySpark when you move to the next tutorial
