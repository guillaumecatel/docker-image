include .env

up:
	docker network create ${TRAEFIK_NETWORK} || true
	docker-compose up -d
	docker-compose -f sample-website/docker-compose.yml --env-file .env  up -d

down:
	docker-compose down
	docker-compose -f sample-website/docker-compose.yml  --env-file .env down
	docker network rm ${TRAEFIK_NETWORK} || true
