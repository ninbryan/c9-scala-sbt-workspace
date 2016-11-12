# Scala Workspace

scala workspace project
loosely based on [this repo](https://github.com/umhan35/c9-scala)

## Setup JDK 8

According to [a post](http://askubuntu.com/questions/464755/how-to-install-openjdk-8-on-14-04-lts)
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

## Setup Scala 2.12.0
```sh
cd /tmp
rm *deb
wget http://downloads.lightbend.com/scala/2.12.0/scala-2.12.0.deb
sudo dpkg -i scala-2.12.0.deb
rm *deb
cd ~/workspace

# scala done

```

## Setup SBT
```sh
sudo apt-get install --force-yes -y apt-transport-https
echo "deb https://dl.bintray.com/sbt/debian /" | sudo tee -a /etc/apt/sources.list.d/sbt.list
sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv 642AC823
sudo apt-get update
sudo apt-get install -y sbt
sudo apt-get update

# sbt done

```
