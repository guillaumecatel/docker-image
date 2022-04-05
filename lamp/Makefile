include .env

up:
	docker-compose up -d --build

down:
	docker-compose down

install: up
	docker exec --env-file .env	-it ${APP_NAME}-${PHP_VERSION} composer install

clean:
	docker-compose rm -v -f -s webserver database phpmyadmin

shell:
	docker exec -it ${APP_NAME}-${PHP_VERSION} /bin/bash
