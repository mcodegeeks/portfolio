### Build
```
$ docker-compose build                  # Build or rebuild services.
```

### Execute
```
$ docker-compose exec                   # Execute a command in a running container
$ docker-compose exec web /bin/bash
$ docker-compose exec web python manage.py createsuperuser
$ docker-compose exec web python manage.py migrate
$ docker-compose exec db psql --username='postgres' --dbname='portfolio'
$ docker-compose exec nginx ls /var/www
```

### Service
```
$ docker-compose up -d                  # Builds, (re)creates, starts, and attaches to containers for a service.
$ docker-compose up --build
$ docker-compose up --no-build
$ docker-compose up --no-start
$ docker-compose up -d db
$ docker-compose up web
$ docker-compose -f docker-compose.prod.yml up -d
```
```
$ docker-compose down                   # Stops containers and removes containers, networks, volumes, and images created by `up`.
$ docker-compose down --rmi all
$ docker-compose down --rmi local
$ docker-compose -f docker-compose.prod.yml down --rmi all
```
```
$ docker-compose stop                   # Stop running containers without removing them.
$ docker-compose stop web
```