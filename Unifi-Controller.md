# Unifi Controller

### Create Docker Volume
  - `docker volume create unifi_data`

### Quick Start Unifi Controller Container
  - `docker run -d --rm --init -p 8080:8080 -p 8443:8443 -p 8843:8843 -p 8880:8880 -p 3478:3478/udp -e TZ='Asia/Shanghai' -e JVM_MAX_HEAP_SIZE=1024M -v unifi_data:/unifi --name UniFi jacobalberty/unifi:stable`
