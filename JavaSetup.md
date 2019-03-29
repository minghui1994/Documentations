<h1>Setting up JAVA in Ubuntu</h1>

Reference: [Linode](https://www.linode.com/docs/development/java/install-java-on-ubuntu-16-04/) 

<h2>Part 1: Before you begin</h2>

|Step|Command             |Description  |
|----|--------------------|-------------|
|1   |sudo apt-get update |update system|
|2   |sudo apt-get upgrade|update system|

<br>

<h2>Part 2: Install Oracle JDK</h2>

|Step|Command                                                |Description                                                                        |    
|----|-------------------------------------------------------|-----------------------------------------------------------------------------------|
|1   |sudo apt-get install software-properties-common|Install software-properties-common, provides and easier way to add new repositories|
|2   |sudo add-apt-repository ppa:webupd8team/java   |Add Java PPA. Note: This repository is not maintained by Oracle                    |
|3   |sudo apt-get update                                    |Update local package cache                                                         |
|4   |sudo apt-get install oracle-java8-installer    |Install metapackage, run an installer for Oracle JDK 8. Java 8 is more suited for development|
|5   |java -version                                          |Check java version|
|6   |javac -version                                         |Check java compiler version|
|7   |sudo add-apt-repository -r ppa:webupd8team/java|PPA only provide installer, not update for JDK itself, can delete once done.|

<br>

<h2>Part 3: Set JAVA Home Environment</h2>

|Step|Command|Description|
|----|-------|-----------|
|1   |echo "JAVA_HOME=$(which java)" l sudo tee -a /etc/environment|To set variable for your system. **NOTE**: Replace l with a line symbol|
|2   |source /etc/environment|Reload system's environment variables.|
|3   |echo $JAVA_HOME|Verify the variable is set correctly.|