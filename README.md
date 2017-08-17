# eJabberd

eJabberd XMPP server

[![Docker Build Status](https://img.shields.io/docker/build/sfoxdev/ejabberd.svg?style=flat-square)]()
[![Docker Build Status](https://img.shields.io/docker/automated/sfoxdev/ejabberd.svg?style=flat-square)]()
[![Docker Build Status](https://img.shields.io/docker/pulls/sfoxdev/ejabberd.svg?style=flat-square)]()
[![Docker Build Status](https://img.shields.io/docker/stars/sfoxdev/ejabberd.svg?style=flat-square)]()

## Usage

### Run Movim
```
docker run -d -u root -p 4560:4560 -p 5222:5222 -p 5269:5269 -p 5280:5280 -p 5443:5443 --net=prosody_network --name example.com sfoxdev/ejabberd
```

### If you forget adminpassword you can change it
```
docker exec -it example.com /bin/bash
# erl
Erlang/OTP 17 [erts-6.2] [source] [64-bit] [smp:2:2] [async-threads:10] [kernel-poll:false]

Eshell V6.2  (abort with ^G)
1> ejabberd_auth:set_password("admin", "example.com", "admin")
```
