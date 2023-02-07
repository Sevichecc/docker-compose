```bash
sudo git clone https://github.com/MaxLeiter/Drift
cd Drift

# edit the docker-compose.yml
sudo vim docker-compose.yml

#build images and up
sudo docker compose build && sudo docker compose up -d

#up
```

generate secret:

```bash
openssl rand -hex 32
```
