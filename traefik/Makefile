include .env

up:
	docker network create web
	docker-compose up -d

down:
	docker-compose down
	docker network rm web

