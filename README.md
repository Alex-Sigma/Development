# DevOps

My process:
At first the required filing system was created:
mkdir multi-container-app
cd multi-container-app
touch docker-compose.yml

Than I have prompted the docker-compose.yml
The final vesion of the docker compose is not the original one. I have faced the problems with trying to scale by using the command docker-compose up -d --scale web=3.

It did work out only after including the traefik into docker-compose.yml. It has solved the problem with local host addresses assignment.

The commands like -compose up -d and the docker-compose up -d --scale web=3 function with no problems.
By using the docker network -ls and docker volume -ls inspect my networks and volumes.

In addition I also got inside of my postgres database by using the docker exec -it multi-container-app-web-1 /bin/bash

Lastly the docker-compose was used to check the state of my containers.
