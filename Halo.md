# Halo

### Create Docker Volume
  - `docker volume create halo_data`

### Quick Start Zerotier Container
  - `docker run -it -d --name Halo -p 8090:8090 -v halo_data:/root/.halo --link MariaDB:db --restart=always halohub/halo:1.4.7`

### Install Halo
  > Database Host must be `db`
