# SmartDNS
> Only the `/smartdns/smartdns.conf` file is valid in `ghostry/smartdns` of Docker.

### Command:
`docker run -d --name smartdns -p 10.12.1.1:53:53 -p 10.12.1.1:53:53/udp -e TZ=Asia/Shanghai -v smartdns_data:/smartdns --restart=unless-stopped ghostry/smartdns:v2020.09.08`
