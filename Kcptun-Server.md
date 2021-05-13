# Kcptun Server

### Create Docker Volume
  - `docker volume create kcptun_data`

### Crate Config File & Paste Config Value
```
{
  "listen": ":29900",
  "target": "172.17.0.1:30936",
  "key": "this_is_test_kcptun_key",
  "crypt": "none",
  "mode": "fast3",
  "mtu": 1350,
  "sndwnd": 512,
  "rcvwnd": 1024,
  "datashard": 10,
  "parityshard": 3,
  "dscp": 0,
  "nocomp": true,
  "quiet": false,
  "tcp": false
}
```
  - create config file: `/var/lib/docker/volumes/kcptun_data/_data/server.json`
  - paste config value to config file.

### Quick Start KcpTun Server Container
  - `docker run -d --name KcptunServer -p 29900:29900/udp -v kcptun_data:/data --restart=unless-stopped xtaci/kcptun:v20210103 server -c /data/server.json`
