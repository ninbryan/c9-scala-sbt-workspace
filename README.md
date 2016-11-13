# Cloud9 Scala SBT Workspace

Cloud9 workspace with Java 8, Scala 2.12.0, and SBT
based on [this repo](https://github.com/umhan35/c9-scala)

## Setup JDK 8

Scala 2.12.0 requires Java 8,
so follow installation according to [this post](http://askubuntu.com/questions/464755/how-to-install-openjdk-8-on-14-04-lts)

```sh
# Installing JDK 8
sudo add-apt-repository ppa:webupd8team/java -y
sudo apt-get update
sudo apt-get install oracle-java8-installer -y

# To automatically set up the Java 8 environment variables
sudo apt-get install oracle-java8-set-default -y

# Check it
java -version

# java done

```

During the process, you will need to confirm the License Agreement

```sh
Oracle Binary Code License Agreement...

[More] # click enter
...
Do you accept the Oracle Binary Code license terms? # type 'Y' then click enter
...
```

## Setup Scala 2.12.0

Installing Scala is more straightforward.

```sh
cd /tmp
rm *deb
# downloading scala
wget http://downloads.lightbend.com/scala/2.12.0/scala-2.12.0.deb
# installing scala
sudo dpkg -i scala-2.12.0.deb
# removing downloaded file
rm *deb
cd ~/workspace

# check it
scala -version

# scala done

```

## Setup SBT 0.13

Installing SBT seems forceful and straightforward

```sh

sudo apt-get install --force-yes -y apt-transport-https
echo "deb https://dl.bintray.com/sbt/debian /" | sudo tee -a /etc/apt/sources.list.d/sbt.list
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 642AC823
sudo apt-get update
sudo apt-get install -y sbt
sudo apt-get update

# sbt done

```

Test out SBT by following the [Hello World example](http://www.scala-sbt.org/0.13/docs/Hello.html)