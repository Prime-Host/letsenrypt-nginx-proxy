# letsenrypt-nginx-proxy

First make sure you have the newest version of all images.


```bash
docker pull nginx
docker pull jwilder/docker-gen
docker pull jrcs/letsencrypt-nginx-proxy-companion
```

Clone the Repo and start all containers.

```bash
git clone https://github.com/Prime-Host/letsenrypt-nginx-proxy.git
docker-compose -f letsenrypt-nginx-proxy/docker-compose.yml up -d
rm -r letsenrypt-nginx-proxy
```
