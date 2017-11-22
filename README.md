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
