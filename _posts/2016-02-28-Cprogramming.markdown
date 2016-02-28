---
layout: post
title:  "C Programming"
date:   2016-02-10 1:20:00 +0300
categories: jekyll update
---
the most important libraries in C:
```#include <stdio.h>```

```#include <stdlib.h>```

```#include <stdbool.h>```

```#include <stdint.h>```

```#include <string.h>```

some network libraries:

```#include <sys/socket.h>``` used for socket programming and its core functions are:

- ```int accept (int socket, struct sockaddr *address,
                                 socklen_t *address_len);```

- ```int socket(int domain, int type, int protocol);```

- ```int bind(int socket, const struct sockaddr *address,
     socklen_t address_len);``` socket
Specifies the file descriptor of the socket to be bound.
address
Points to a sockaddr structure containing the address to be bound to the socket. The length and format of the address depend on the address family of the socket.
address_len
Specifies the length of the sockaddr structure pointed to by the address argument.

- ```int listen(int socket, int backlog);``` The listen() function marks a connection-mode socket, specified by the socket argument, as accepting connections, and limits the number of outstanding connections in the socket's listen queue to the value specified by the backlog argument.
