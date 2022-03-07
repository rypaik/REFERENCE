Buidling Docker Image

https://docs.docker.com/samples/postgresql_service/





RUN COMMAND

$ sudo docker-compose run web django-admin startproject composeexample .







Running Docker 

if docker-compose file is namded docker-compose.yml

`docker-compose up`

- compose app has the `manage.py runserver` command



to shutdown 

`docker-compose down`





if named anotehr file

this combines a buiild command

docker-compose -f <docker-compose name> up  -d --build



TRY - NOTE -d id detached mode

docker-compose -f <docker-compose> up -d         





can also run bash in individual containers

docker exec -it <container_name> bash



can you `/bin/sh` if no bash