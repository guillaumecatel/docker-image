include .env

up:
	docker network create ${TRAEFIK_NETWORK} || true
	docker-compose up -d

down:
	docker-compose down

