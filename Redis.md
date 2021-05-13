# Redis

### Create Docker Volume
  - `docker volume create redis_data`

### Quick Start Redis Container
  - `docker run -d --name=Redis -p 127.0.0.1:6379:6379 --restart=unless-stopped -v redis_data:/data redis:6.2.1`
