# Install Apache Pig on Centos 7

## 1) Download appropriate version of Pig

Chage user to "hadoop" and downlaod Pig archive (from https://pig.apache.org/releases.html) to home directory of "hadoop" user. Choose the Hive version that is copatible with currently installed Hadoop version.
```
su - hadoop
wget http://www-eu.apache.org/dist/pig/pig-0.16.0/pig-0.16.0.tar.gz
```

## 2) Extract archive 
```
tar -xvf pig-0.16.0.tar.gz
```

## 3) Edit .bash_profile of "hadoop" user
```
vi .bash_profile
```
add following settings:
```
export PIG_INSTALL=/home/hadoop/pig-0.16.0
export PATH=$PATH:/home/hadoop/pig-0.16.0/bin
```
to apply changes:
```
source .bash_profile
```
## 6) Congratulation! Its Done...
to check Pig version
```
pig --version
```
use `pig` to start Pig interpreter
