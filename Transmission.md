# Transmission

### Quick Start Transmission Container
  - `docker run -d --name "Transmission" --restart=always -p "10.12.1.1:51413":51413/udp -p "10.12.1.1:51413":51413/tcp -p "10.12.1.1:9091":9091/tcp -h "OrasTransmission" -e TZ:"Asia/Shanghai" -e "TRANSMISSION_WEB_HOME":"/transmission-web-control" -e "USER":"admin" -e "PASS":"admin" -e "PGID":"1000" -e "PUID":"1000" -v TDTransmissionConfig:/config -v TDTransmission:/downloads -v NASMountTransmission:/downloads/NAS -v TDTransmissionWatch:/watch linuxserver/transmission`
