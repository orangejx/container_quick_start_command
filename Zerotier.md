# Zerotier

### Create Docker Volume
  - `docker volume create zerotier_data`

### Quick Start Zerotier Container
  - `docker run -d --name Zerotier \
--net=host \
--device=/dev/net/tun \
--cap-add=NET_ADMIN \
--cap-add=SYS_ADMIN \
-v zerotier_data:/var/lib/zerotier-one \
--restart=unless-stopped \
bltavares/zerotier:1.6.2-2`

### Join Zerotier Network
> `8056c2e21c000001` is your zerotier network id.

  - `docker exec Zerotier /zerotier-cli join 8056c2e21c000001`
  or
  - `mkdir /var/lib/docker/volumes/zerotier_data/_data/networks.d/ && touch /var/lib/docker/volumes/zerotier_data/_data/networks.d/8056c2e21c000001.conf`
