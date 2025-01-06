curl -sSL https://ngrok-agent.s3.amazonaws.com/ngrok.asc \
	| sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null \
	&& echo "deb https://ngrok-agent.s3.amazonaws.com buster main" \
	| sudo tee /etc/apt/sources.list.d/ngrok.list \
	&& sudo apt update \
	&& sudo apt install ngrok


ngrok http http://localhost:8080



ngrok config add-authtoken 2rFlVYhFwN1a5keuKqS0S54iRco_7Pve5ktCzxYRGDYhz4VFL



ngrok tunnel --label edge=edghts_2rFq7m0Tv1DRZLrPeccKZqv4VCE http://localhost:80
