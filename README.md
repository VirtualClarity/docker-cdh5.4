Creating docker with all CDH components
=========================================

Docker scripts in this directory spawns a CentOS 6 docker VM and installs all the CDH components (Hadoop, Spark, Hbase, Hive, Impala, Hue, Zookeeper, Oozie etc.).


## How to build the cdh container?

```bash
docker build -t docker-cdh54 .
```

## How to run the cdh container?
Use the bash script provided

Wait a little as the build can take several minute to download each image and packages to rebuild CDH.

## How to open an ssh session inside the cdh?
```bash
docker ps
```
the command return the list of Containers. Select the Container ID matching the CDH container that was started.
=> 922ac2f47d93 ... or any similar Container Id

```bash
docker attach 922ac2f47d93
```
