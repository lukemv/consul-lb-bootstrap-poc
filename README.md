This proof of concept illustrates bootstrapping a consul server cluster via a TCP load balancer



**Compose up**

```
$ docker-compose build
$ docker-compose up -d
$ docker-compose logs -f
```



**Scaling up:** *(in another console session)*

```
$ docker-compose scale consul-server=5
$ docker exec -it consul_consul-server_1 /bin/sh
$ consul members
```


**Scaling down:**

```
$ docker-compose scale consul-server=3
$ docker exec -it consul_consul-server_1 /bin/sh
$ consul members
```

