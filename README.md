## without docker-compose.yml

### Owncast

```bash
sudo docker run -d -v /opt/owncast/data:/app/data -p 8080:8080 -p 1935:1935 -it gabekangas/owncast:latest --name owncast
```

- [Use a container image - Owncast](https://owncast.online/quickstart/container/)
- [Owncast - Free and Open Source Livestreaming](https://owncast.online/)

### PrivateBin

Location: `/opt/privatebin`

```bash
sudo docker run -d \
  --name privatebin \
  --restart="always" \
  --read-only \
  -p 8040:8080 \
  -v /opt/privatebin/privatebin-data:/srv/data privatebin/nginx-fpm-alpine
```

[privatebin/nginx-fpm-alpine - Docker Image | Docker Hub](https://hub.docker.com/r/privatebin/nginx-fpm-alpine/)

### LittleLink

```bash
docker run --detach \
    --name littlelink-custom \
    --hostname littlelink-custom \
    --env HTTP_SERVER_NAME="yourwebsite.org" \
    --env HTTPS_SERVER_NAME=yourwebsite.org" \
    --env SERVER_ADMIN="your@email.org" \
    --env TZ="Europe/Berlin" \
    --env PHP_MEMORY_LIMIT="512M" \
    --env UPLOAD_MAX_FILESIZE="50M" \
    --publish 80:80 \
    --publish 447:443 \
    --restart unless-stopped \
    --mount source=llc,target=/htdocs \
    julianprieber/littlelink-custom
```

[LittleLink Custom - A self-hosted open-source Linktree alternative](https://littlelink-custom.com/)
