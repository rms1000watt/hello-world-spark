# 1. Add File

## Prerequisites

- From a fresh starting point, start `spark-hadoop` as shown under `Usage > Starting the Container` in the Readme.md

## Tutorial

```bash
# Access bash in the container
docker exec -it spark-hadoop /bin/bash

# Create a folder in hadoop
hdfs dfs -mkdir /user/root/test-data

# Create a file in the container
cat << EOF > test1.txt
This is a test file
with multiline contents
to test with.
EOF

# Add the file to hadoop
hdfs dfs -put test1.txt /user/root/test-data

# View the files in hadoop
hdfs dfs -ls /user/root/test-data

# View the file contents in hadoop
hdfs dfs -cat /user/root/test-data/test1.txt

# Leave bash
exit
```

## Notes

You can also view the files in hadoop by going to the web UI:

- Go to `http://localhost:50070`
- Click `Utilities` on top right menu
- Click `Browse the file system` on that drop down
- Now you can type in paths in the search bar or click through directories

*Gotcha*: Downloading files from the web UI fails since it does a redirect from `localhost` to the node that contains the data. If hadoop wasn't running in docker--it would be a seamless experience.
