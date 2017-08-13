# Hello World Spark

The foundation of the project was taken from [github.com/sequenceiq/docker-spark](https://github.com/sequenceiq/docker-spark)

## Introduction

TODO

## Contents

- Usage

### Usage

```bash
# Start Spark + Hadoop
nohup bash -c "sleep 45; open http://localhost:8088; open http://localhost:8042" &> /dev/null &
docker rm spark-hadoop
docker run -itd -p 8088:8088 -p 8042:8042 -p 4040:4040 --name spark-hadoop sequenceiq/spark:1.6.0 bash

# TTY into the container
docker exec -it spark-hadoop /bin/bash

# Stop the container
docker stop spark-hadoop
```
