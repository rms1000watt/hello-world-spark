# Hello World Spark

The foundation of the project was taken from [github.com/gettyimages/docker-spark](https://github.com/gettyimages/docker-spark)

## Introduction

TODO

## Contents

- Usage

### Usage

```bash
# Start Spark
docker-compose up -d

# View the Spark UI
open http://localhost:8080/

# Play with PySpark
docker exec -it sparknohadoop_master_1 /bin/bash bin/pyspark

# Leave when you're done
exit

# Look around the OS
docker exec -it sparknohadoop_master_1 /bin/bash

# Leave when you're done
exit

# Stop the containers
docker-compose down
```
