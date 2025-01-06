curl -sSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
	| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \
	&& echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
	| sudo tee /etc/apt/sources.list.d/ngrok.list \
	&& sudo apt update \
	&& sudo apt install ngrok


ngrok http http://localhost:8080



ngrok config add-authtoken 2rFlVYhFwN1a5keuKqS0S54iRco_7Pve5ktCzxYRGDYhz4VFL



ngrok tunnel --label edge=edghts_2rFq7m0Tv1DRZLrPeccKZqv4VCE http://localhost:80




debug: false
uuid: 80e68389-c4a3-438a-829a-cd3dc97e1c08
token_id: 4MMWUl3JNz9nyin4
token: 4NOwzmXgHDfI53lklkOLmS745Ao0iVxucG9M8M2Exq0oEBKQ2ToRdRc7HBqnWTJL
api:
  host: 0.0.0.0
  port: 443
  ssl:
    enabled: false
    cert: /etc/letsencrypt/live/touching-heroic-koi.ngrok-free.app/fullchain.pem
    key: /etc/letsencrypt/live/touching-heroic-koi.ngrok-free.app/privkey.pem
  upload_limit: 100
system:
  data: /var/lib/pterodactyl/volumes
  sftp:
    bind_port: 2022
allowed_mounts: []
remote: 'https://reimagined-space-lamp-xjvw9g57vjphp7j9-80.app.github.dev'
