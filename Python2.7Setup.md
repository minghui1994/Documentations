<h1>Python 2.7 Setup</h1>

Reference: [Tech admin](https://tecadmin.net/install-python-2-7-on-ubuntu-and-linuxmint/)

<h2>Part 1: Prerequisites</h2>

Install the required dependencies

|Step|Command|Description|
|----|-------|-----------|
|1|sudo apt-get update|Update system|
|2|sudo apt-get install build-essential checkinstall||
|3|sudo apt-get install libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev||

<br>

<h2>Part 2: Download Python</h2>

|Step|Command|Description|
|----|-------|-----------|
|1|cd /usr/src||
|2|sudo wget https://www.python.org/ftp/python/2.7.15/Python-2.7.15.tgz|Download python 2.7.15|
|3|sudo tar xzf Python-2.7.15.tgz|Extract the downloaded package|

<br>

<h2>Part 3: Compile Python source</h2>

|Step|Command|Description|
|----|-------|-----------|
|1|cd Python-2.7.15||
|2|sudo ./configure --enable-optimizations||
|3|sudo make altinstall||
|4|python2.7 -V|Check version|