# guillaumecatel/docker-images/lamp

> 🐳 Docker configurations and images for LAMP stack with Composer

## Installation

```bash
npx degit guillaumecatel/docker-images/lamp <my-project-name>
cp .env.example .env
make install
```

## Usage

```bash
make install # bootstrap lamp stack and run composer install
make up # bootstrap lamp stack
make down # shutdown lamp stack
make clean # clear lamp stack data
make shell # start server shell
```

## License
MIT
