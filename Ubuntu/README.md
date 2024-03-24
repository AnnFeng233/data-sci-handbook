## Vim syntax

Edit file `sudo vim <file_path/file_name>`, insert mode `i`, command mode Esc key

Exit file 1. press Esc key; 2. `:q` quit, `:q!` quit without saving, `:x` save and quit, `:qa` quit all open file 

## Install java

Update system package `$ sudo apt update`

Install Java `$ sudo apt install default-jkd -y`

See version `$ java -version`

## Install Python and pip

Python `sudo apt-get install python3`

Pip `sudo apt-get install python3-pip`, to install package `pip3 install <package_name>`

Create python env `python3 -m venv myenv`, activate the env `source myenv/bin/activate`, exit `deactivate`

## Install Apache Spark
(java required)

Download file
```
$ sudo apt install curl mlocate git scala -y
$ curl -O https://archive.apache.org/dist/spark/spark-3.2.0/spark-3.2.0-bin-hadoop3.2.tgz
$ sudo tar xvf spark-3.2.0-bin-hadoop3.2.tgz
```

Create installation directory `/opt/spark`
```
$ sudo mkdir /opt/spark
$ sudo mv spark-3.2.0-bin-hadoop3.2/* /opt/spark
$ sudo chmod -R 777 /opt/spark
```

Add installation to system path `$ sudo vim ~/.bashrc`

Add the lines in the end
```
export SPARK_HOME=/opt/spark
export PATH=$PATH:$SPARK_HOME/bin:$SPARK_HOME/sbin
```

Save chage `$ source ~/.bashrc`

To start `$ start-master.sh`, and `$ start-slave.sh`

Finally `spark-shell`

Exit shell `:quit`
