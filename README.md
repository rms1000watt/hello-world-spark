# Hello World Spark

The foundation of the project was taken from (github.com/gettyimages/docker-spark)[https://github.com/gettyimages/docker-spark].

This is a hello world project for Apache Spark to play with some examples

## Introduction

TODO

## Contents

- Usage

### Usage

Start Spark

```bash
# Start Spark
docker-compose up -d

# Play with PySpark
docker exec -it helloworldspark_master_1 /bin/bash bin/pyspark

# Leave when you're done
exit

# Look around the OS
docker exec -it helloworldspark_master_1 /bin/bash

# Leave when you're done
exit
```

## TODO

- [ ] Example using PySpark against linux FS
- [ ] Example using PySpark against HDFS
- [ ] Additional Examples