# guillaumecatel/docker-images/traefik

> 🐳 Docker configurations and images for Traefik reverse proxy

## Installation

```bash
npx degit guillaumecatel/docker-images/traefik <my-project-name>
cp .env.example .env
cp acme.sample.json acme.json
chmod 600 acme.json
make up
# go to your dashboard -> https://traefik.localhost (root/root)

# edit traefik.yml to set the log level and your mail for Let's Encrypt for production
# edit user_credentials for production
```

## Usage

```bash
make up # bootstrap Traefik reverse proxy
make down  # shutdown Traefik reverse proxy
```

## Add service to Traefik
```yml
# add labels and network to your docker-compose.yml
version: '3'
services:
  my_service:
    # ...
    labels:
      - 'traefik.enable=true'
      - 'traefik.http.routers.<my_service_name>.rule=Host(`<my_service_host>`)'
      - 'traefik.http.routers.<my_service_name>.entrypoints=websecure'
      - 'traefik.http.routers.<my_service_name>.tls.certresolver=lets-encr'

networks:
  default:
    external:
      name: '<my_traefik_network_name>'
```

## License
MIT
