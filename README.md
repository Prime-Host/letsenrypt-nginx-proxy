# letsenrypt-nginx-proxy

First make sure you have the newest version of all images.


```bash
docker pull nginx
docker pull jwilder/docker-gen
docker pull jrcs/letsencrypt-nginx-proxy-companion
```

Clone the Repo and start all containers.

```bash
MY_EXTERNAL_IP=$(ip addr show eth0 | awk '$1 == "inet" {gsub(/\/.*$/, "", $2); print $2}')
```
