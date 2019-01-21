
# Instalação do laravel lab

- Criação do projeto
```
docker run -it --rm \
    -v $(pwd):/app luanpereiranc/docker-laravel \
    composer create-project laravel/laravel app
```

- Colocando pra funcionar
```
docker run -p 8080:80 \
    -v $(pwd)/app:/app \
    --name webserver \
    -d luanpereiranc/docker-laravel
```