# bWAPP instances for Slow HTTP DoS testing 
DC7494 Meetup #4

## build & run

```
docker-compose build
docker-compose up
curl http://localhost:PORT/install.php?install=yes # once for bWAPP init
```

## testing 

using [slowhttptest](https://github.com/shekyan/slowhttptest):

```
slowhttptest -u http://localhost:PORT/login.php {-H,-B,-R,-X} {params} 
```

## test instances

apache2-vulnerable: http://localhost:8081/login.php

apache2-fixed: http://localhost:8082/login.php

nginx-vulnerable: http://localhost:9081/login.php

nginx-fixed: http://localhost:9082/login.php
