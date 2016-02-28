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

- ```int socket(int domain, int type, int protocol);```

server functions:

- ```int bind(int socket, const struct sockaddr *address, socklen_t address_len);```

- ```int listen(int socket, int backlog);```

- ```int accept (int socket, struct sockaddr *address, socklen_t *address_len);```

-```ssize_t recv(int socket, void *buffer, size_t length, int flags);```

Client functions:

-```int connect(int socket, const struct sockaddr *address,socklen_t address_len);```

-```ssize_t send(int socket, const void *buffer, size_t length, int flags);```

see [<sys/socket.h>][<sys/socket.h>] for more informations.

--------------------------------------------------------------------------------------------

```#include <arpa/inet.h>``` contains the in_addr structure and has the following functions:

- ```uint32_t htonl(uint32_t);```

- ```uint16_t htons(uint16_t);```

- ```uint32_t ntohl(uint32_t);```

- ```uint16_t ntohs(uint16_t);```

these functions are used for big and little endian conversions.

[<sys/socket.h>]:http://pubs.opengroup.org/onlinepubs/7908799/xns/syssocket.h.html
