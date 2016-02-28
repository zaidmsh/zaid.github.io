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

--------------------------------------------------------------------------------------------
PostgreSQL is an open DBMS. The [postgres][postgres] application for Mac OS X is a good and easy way to deal with postgreSQL DB.

```#include <libpq-fe.h>``` is a C library for the PostgreSQL databases:

- ```PGconn *PQconnectdb(const char *conninfo);``` is used to connect to a database for example ```PQconnectdb("postgresql://zaid@localhost/zaid");``` which returns a handler of type ```PQconn``` and takes the specified parameters the first ```zaid``` mean the user. ```localhost``` represent the server in which thee database is located in.``` zaid``` is the name of the database. ```PGconn *PQconnectdbParams(const char **keywords, const char **values, int expand_dbname);``` is the succerssor of PQconnectdb for more information about it visit [PosetgreSQL Databese-connection][PosetgreSQL-Databese-connection]


- ```void PQfinish(PGconn *conn);``` closes the connection to the database.

- There are functions used to check the status of the connection which are very important and can be found in [here][PostgreSQL-conn-status].

- ```PGresult *PQexec(PGconn *conn, const char *command);``` returns a PGresult after executing the command given in the parameter. ```PGresult *PQexecParams(PGconn *conn,
                       const char *command,
                       int nParams,
                       const Oid *paramTypes,
                       const char * const *paramValues,
                       const int *paramLengths,
                       const int *paramFormats,
                       int resultFormat);``` this is the extended version of the PQexec which you can find more information about [here][PQexecParams].


[<sys/socket.h>]: http://pubs.opengroup.org/onlinepubs/7908799/xns/syssocket.h.html
[postgres]: http://postgresapp.com/
[PosetgreSQL-Databese-connection]: http://www.postgresql.org/docs/9.1/static/libpq-connect.html
[PostgreSQL-conn-status]: http://www.postgresql.org/docs/9.1/static/libpq-status.html
[PQexecParams]: http://www.postgresql.org/docs/9.1/static/libpq-exec.html
