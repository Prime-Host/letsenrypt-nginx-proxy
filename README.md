# letsenrypt-nginx-proxy

Clone the Repo

```bash
git clone https://github.com/Prime-Host/letsenrypt-nginx-proxy.git
cd letsenrypt-nginx-proxy
```

With this command you can find out yor external IP address. Replace 0.0.0.0 in env-sample with your IP.
```bash
ip addr show eth0 | awk '$1 == "inet" {gsub(/\/.*$/, "", $2); print $2}'
```

To start all containers run this script:
```bash
./run.sh
```

git clone https://github.com/evertramos/docker-compose-letsencrypt-nginx-proxy-companion.git
mv .env.sample .env
PROXY_IP_DOCKER=$(ip addr show ens18 | awk '$1 == "inet" {gsub(/\/.*$/, "", $2); print $2}')
sed -i "s/0.0.0.0/$PROXY_IP_DOCKER/g" .env
./start.sh
