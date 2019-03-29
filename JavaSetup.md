<h1>Setting up JAVA in Ubuntu</h1>


<h2>Part 1: Before you begin</h2>

|Step|Command             |Description  |
|----|--------------------|-------------|
|1   |sudo apt-get update |update system|
|2   |sudo apt-get upgrade|update system|

<br>

<h2>Part 2: Install Oracle JDK</h2>

|Step|Command                                                |Description                                                                        |    
|----|-------------------------------------------------------|-----------------------------------------------------------------------------------|
|1   |sudo apt-get install (space) software-properties-common|Install software-properties-common, provides and easier way to add new repositories|
|2   |sudo add-apt-repository (space) ppa:webupd8team/java   |Add Java PPA. Note: This repository is not maintained by Oracle                    |
|3   |sudo apt-get update                                    |Update local package cache                                                         |
|4   |sudo apt-get install (space) oracle-java8-installer    |Install metapackage, run an installer for Oracle JDK 8. Java 8 is more suited for development|
|5   |java -version                                          |Check java version|
|6   |javac -version                                         |Check java compiler version|
|7   |sudo add-apt-repository (space) -r (space) ppa:webupd8team/java|PPA only provide installer, not update for JDK itself, can delete once done.|

<br>

<h2>Part 3: Set JAVA Home Environment</h2>

