# Rideeze Web App

Make sure you have access to the [rideeze organization](https://hub.docker.com/u/rideeze/dashboard/) on Docker Hub 
with your account:
    $ docker login
    
Launch the development stack:
    $ docker-compose up -d postgresql redis
    $ docker-compose up -d rideeze-web
   
If you're cloning the project for the first time (and did setup the database using pg_restore), then:

    $ docker-compose run --rm shell  "python manage.py migrate"


# Docker build

    - docker build -t rideeze/rideeze-web .
