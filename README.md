
Docker-compose Base Linux、Nginx(Openresty)、MySQL5.7、PHP7(PHP-FPM)
#### ThinkPHP5.1 部署
* 启动服务
    ```
    docker-lnmp\dev\nginx\v1.1> docker-compose up
    ```
* 浏览器输入：`http://127.0.0.1:8088/index/index/hello`
* 停止重启
```
$ docker-lnmp\dev\nginx\v1.1> docker-compose restart
Restarting lnmp-nginx-alpine ... done
Restarting lnmp-php7.2.13    ... done
$ docker-lnmp\dev\nginx\v1.1> docker-compose stop
Stopping lnmp-nginx-alpine ... done
Stopping lnmp-php7.2.13    ... done
$ docker-lnmp\dev\nginx\v1.1> docker-compose ps
 Name                    Command             State    Ports
```

支持Https: `https://127.0.0.1:8088/`

#### 因为相比`nginx:latest`，`nginx:alpine`有几点优势：
* 用的是最新版nginx镜像，功能与`nginx:latest`一模一样
* alpine 镜像用的是[Alpine Linux](https://alpinelinux.org/)内核，比ubuntu内核要小很多。
* `nginx:alpine` 默认支持http2。

## HELP
* [Dockerise your PHP application with Nginx and PHP7-FPM](http://geekyplatypus.com/dockerise-your-php-application-with-nginx-and-php7-fpm/)
* [docker-openresty](https://github.com/openresty/docker-openresty)



ERROR: for nginx  Cannot start service nginx: OCI runtime create failed: container_linux.go:348: