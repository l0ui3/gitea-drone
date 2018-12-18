# [Docker-Compose] Gitea, Drone & Traefik

Run Gitea, Drone in Docker, and reverse proxy with Traefik.

## Usage

1. First create a docker network named `gitea-network`:
```sh
$ docker network create gitea-network
```

2. Change `your-domain.com` in `docker-compose.yml` and `gitea-app.ini` to your domain.

3. Run those services
```sh
$ docker-compose up -d
```

**Exposed Services**
- Gitea: http://your-domain.com/git
- Gitea-SSH: your-domain.com:2222
- Drone: http://your-domain.com:81
- Traefik Web UI: http://localhost:8081
