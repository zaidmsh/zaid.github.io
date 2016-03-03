---
layout: post
title:  "Linux Commands"
date:   2016-03-03 11:30:00 +0300
categories: Linux cli
---
## Process Related Commands

    $ ps aux

    USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
    root         1  0.0  0.2  19232  1496 ?        Ss   08:09   0:00 /sbin/init
    root      2416  0.0  0.7  97900  3884 ?        Ss   08:21   0:00 sshd: vagrant [priv]
    vagrant   2419  0.0  0.4  97900  2212 ?        S    08:21   0:00 sshd: vagrant@pts/0
    vagrant   2420  0.0  0.3 108304  1868 pts/0    Ss   08:21   0:00 -bash
    vagrant   2449  4.0  0.2 110232  1172 pts/0    R+   08:34   0:00 ps aux


## Archive Handling

How to unarchive:

    $ tar -xzvf archive.tar.gz
    # x = extract
    # z = compress
    # v = view
    # f = file name

How to archive:

    $ tar -czvf archive.tar.gz archive/
    # c = create
