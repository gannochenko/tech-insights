# Docker

* [Docker volumes](https://www.linux.com/learn/docker-volumes-and-networks-compose)

How to run a dockerized app knowing its image name:
~~~~
docker run -p 5432:5432 -d postgres:10
~~~~

How to build an image from the Dockerfile in the current folder
~~~~
docker build -t container-name .
~~~~

How to run the container interactively
~~~~
docker run -it container-name /bin/bash
~~~~

How to see all containers running
~~~~
docker ps
~~~~

How to enter the tty session on the running container
~~~~
docker exec -it container-id /bin/bash
~~~~

How to stop the container
~~~~
docker stop container-id
~~~~

How to stop continiously restarting container
~~~~
docker update --restart=no container-id
~~~~

How to prune the entire system
~~~~
docker system prune -a
~~~~
