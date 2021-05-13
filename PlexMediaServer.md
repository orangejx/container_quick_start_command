# PlexMediaServer

`docker run -d --name PlexMediaServer --restart=always -p 10.12.1.1:1900:1900/udp -p 10.12.1.1:32410-32414:32410-32414/udp -p 10.12.1.1:3005:3005/tcp -p 10.12.1.1:8324:8324/tcp -p 10.12.1.1:32400:32400/tcp -p 10.12.1.1:32469:32469/tcp -e TZ="Asia/Shanghai" -e PLEX_CLAIM="claim-this-is-test-plex-claim" -e ADVERTISE_IP="http://10.12.1.1:32400" -e PLEX_UID="1001" -e PLEX_GID="1001" -e CHANGE_CONFIG_DIR_OWNERSHIP="False" -e ALLOWED_NETWORKS="172.16.0.0/12" -h Oras -v TDPMS:/config -v TDPMS:/transcode -v TDPMSData:/data -v NASMountPMS:/data/NAS plexinc/pms-docker`
