# hadoop-configs

Maintaining my hadoop configs for open source apache hadoop compilation

### env
> export HADOOP_CONF_DIR=/hadoop/etc/hadoop

> export HADOOP_PREFIX=/home/sanjeevt/Projects/hadoop/hadoop-dist/target/hadoop-3.0.0-SNAPSHOT
 
> export PATH=$PATH:$HADOOP_PREFIX/bin:$HADOOP_PREFIX/sbin

> 


### starting
> hdfs namenode -format san_hdfs ## one time only

> hdfs --daemon  start  namenode
> 
> hdfs --daemon  start  datanode
> 
> 
> yarn --daemon start resourcemanager
> 
> yarn --daemon start nodemanager
> 
> 
> mapred --daemon start historyserver


### hdfs directories
> hadoop fs -mkdir /hadoop/logs
> 
> hadoop fs -mkdir /user/sanjeevt
> 
> hadoop fs -mkdir -p /tmp
> 
> hdfs dfs -chmod 1777  /tmp

### local directories
> mkdir -p /hadoop/{hdfs,yarn}
> 
> mkdir -p /hadoop/hdfs/{name,data}
> 
> mkdir -p /hadoop/hdfs/data/d{1,2,3}
> 
> mkdir -p /hadoop/yarn/{rmstore,local,logs}
> 
> mkdir -p /hadoop/yarn/local/l{1,2,3}
> 
> mkdir -p /hadoop/yarn/logs/l{1,2,3}
> 

### acess
> NN http://192.168.156.10:50070/dfshealth.html
> 
> RM http://192.168.156.10:8088/cluster
>
> Run Sample
> 
> hadoop jar $HADOOP_PREFIX/share/hadoop/mapreduce/hadoop-mapreduce-examples-3.0.0-SNAPSHOT.jar pi 500 40
> 
> Check if scheduled
> http://192.168.156.10:8088/cluster/scheduler
