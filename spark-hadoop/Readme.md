# Hello World Spark

The foundation of the project was taken from [github.com/sequenceiq/docker-spark](https://github.com/sequenceiq/docker-spark)

## Introduction

TODO

## Contents

- Usage
- Tutorials

## Usage

### Starting the Container

```bash
# Start Spark + Hadoop
docker run -itd -p 8088:8088 -p 8042:8042 -p 4040:4040 -p 50070:50070 -p 50075:50075 --name spark-hadoop sequenceiq/spark:1.6.0 bash
```

### View the web UIs

After the container comes up and initializes, you can view the web UIs at:

- [http://localhost:8088](http://localhost:8088)
- [http://localhost:8042](http://localhost:8042)
- [http://localhost:50070](http://localhost:50070)

### Accessing the Container

```bash
# Run bash in the container
docker exec -it spark-hadoop /bin/bash

# Exit the container
exit
```

### Cleanup

```bash
# Stop the container
docker stop spark-hadoop

# Remove the container
docker rm spark-hadoop
```

## Tutorials

Tutorials are available under the `tutorials` folder. Here is a list of tutorials:

- `1-add-file.md`
- `2-pyspark-read-file.md`
- `3-pyspark-manipulate-file.md`
