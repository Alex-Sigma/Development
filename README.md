# DevOps

What was my process first i have created the required filing system:
mkdir multi-container-app
cd multi-container-app
touch docker-compose.yml

The final vesion of the docker compose is not the oroginal one. I have faced the problem with trying to scale by usinf the command docker-compose up -d --scale web=3.

It did work out and the scaling functions the traefik picks the available adresses.

The commands like -compose up -d and the docker-compose up -d --scale web=3 function with no problems.
By using the docker network -ls and docker volume -ls inspect my networks and volumes.

In addition I also hot insideby my postgres data by using the docker exec -it multi-container-app-web-1 /bin/bash

Lastly the docker-compose was used to check the state of my containers.
