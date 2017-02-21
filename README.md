# letsenrypt-nginx-proxy

Run these commands to start the containers.


```bash
docker pull jwilder/nginx-proxy
docker pull jrcs/letsencrypt-nginx-proxy-companion
```


```bash
$ docker run -d -p 80:80 -p 443:443 \
    --name nginx-proxy \
    --restart=always \
    -v /var/docker-data/certs:/etc/nginx/certs:ro \
    -v /etc/nginx/vhost.d \
    -v /usr/share/nginx/html \
    -v /var/run/docker.sock:/tmp/docker.sock:ro \
    jwilder/nginx-proxy
```


```bash
$ docker run -d \
    --name letsenrypt \
    --restart=always \
    -v /var/docker-data/certs:/etc/nginx/certs:rw \
    --volumes-from nginx-proxy \
    -v /var/run/docker.sock:/var/run/docker.sock:ro \
    jrcs/letsencrypt-nginx-proxy-companion
```
