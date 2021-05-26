# Jellyfin

### Quick Start Jellyfin Container
  - `docker run -d --name Jellyfin --restart=always -p 10.12.1.2:1900:1900/udp -p 10.12.1.2:8096:8096/tcp -p 10.12.1.2:8920:8920/tcp -h Jellyfin -v TDJellyfinCache:/cache -v TDJellyfinConfig:/config -v TDJellyfinData:/media -v NASMountJellyfin:/media/NAS jellyfin/jellyfin`
