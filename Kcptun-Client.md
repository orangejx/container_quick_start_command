# Kcptun Client

### Create Docker Volume
> if you already crate the same volume, u can skip this step.

  - `docker volume create kcptun_data`

### Crate Config File & Paste Config Value
```
{
  "localaddr": ":29900",
  "remoteaddr": "1.1.1.1:29900",
  "key": "this_is_test_kcptun_key",
  "crypt": "none",
  "mode": "fast3",
  "mtu": 1350,
  "sndwnd": 1024,
  "rcvwnd": 512,
  "datashard": 10,
  "parityshard": 3,
  "dscp": 0,
  "nocomp": true,
  "quiet": false,
  "tcp": false
}
```
  - create config file: `touch /var/lib/docker/volumes/kcptun_data/_data/client.json`
  - paste config value to config file.

### Quick Start KcpTun Server Container
  - `docker run -d --name KcptunClient -p 29900:29900 -v kcptun_data:/data --restart=unless-stopped xtaci/kcptun:v20210103 client -c /data/client.json`
