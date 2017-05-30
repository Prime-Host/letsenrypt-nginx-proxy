# letsenrypt-nginx-proxy

First make sure you have the newest version.


```bash
docker pull nginx
docker pull jwilder/docker-gen
docker pull jrcs/letsencrypt-nginx-proxy-companion
```

```bash
git clone https://github.com/Prime-Host/letsenrypt-nginx-proxy.git
docker-compose -f letsenrypt-nginx-proxy/docker-compose.yml up -d
rm -r letsenrypt-nginx-proxy
```
