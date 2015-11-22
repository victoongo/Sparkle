# Sparkle
Joyfully distributed. 

### install Java
```
sudo apt-get install openjdk-7-jdk
```

### get Spark binary
```
wget http://d3kbcqa49mib13.cloudfront.net/spark-1.5.2-bin-hadoop2.6.tgz
tar zxf spark-1.5.2-bin-hadoop2.6.tgz
```

### on MAC, add to .bash_profile
```
export PATH="/Users/un/Applications/spark-1.5.0-bin-hadoop2.6/bin:$PATH"

export SPARK_HOME=/Users/un/Applications/spark-1.5.0-bin-hadoop2.6
#export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH
export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/build:$PYTHONPATH
```

### on Ubuntu, add to .bashrc (or .profile)
```
export PATH="/home/un/spark-1.5.2-bin-hadoop2.6/bin:$PATH"

export SPARK_HOME=/home/un/spark-1.5.2-bin-hadoop2.6
#export PYTHONPATH=$SPARK_HOME/python:$PYTHONPATH
export PYTHONPATH=$SPARK_HOME/python:$SPARK_HOME/python/build:$PYTHONPATH
```

### on MAC, start ipython notebook with pyspark like this:
```
IPYTHON_OPTS="notebook" pyspark
```

### on Ubuntu, like this:
```
PYSPARK_DRIVER_PYTHON=ipython PYSPARK_DRIVER_PYTHON_OPTS="notebook" ./bin/pyspark
```

### remote Ubuntu, like this
```
PYSPARK_DRIVER_PYTHON=ipython PYSPARK_DRIVER_PYTHON_OPTS="notebook --pylab inline --no-browser --port=7778" $SPARK_HOME/bin/pyspark
```