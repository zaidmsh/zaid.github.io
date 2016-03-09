---
layout: post
title:  "Hadoop Setup"
date:   2016-03-09 9:45:00 +0300
categories: HADOOP
---
# Install Java

    sudo aptitude install openjdk-7-jdk

# SSH

- Install ssh command

    `sudo aptitude install SSH`
    `sudo aptitude install rsync`

- Generate keys

    `ssh-keygen`

- Execute the following to be able to ssh to localhost without a passphrase

    `ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa`
    `cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys`

- Now ssh to localhost

    `ssh localhost`

# Hadoop Setup

- First download the hadoop gz file.

- Extract the file `hadoop-2.7.2.tar.gz` to : `/home/vagrant/`.

- `vi etc/hadoop/hadoop-env.sh` to specify to hadoop where the java files are located by modifying `export JAVA_HOME=` to `export JAVA_HOME=/usr/lib/jvm/java-7-openjdk-amd64/`.
