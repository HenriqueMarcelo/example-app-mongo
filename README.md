## Primeira utilização do Laravel
Adicone esta linha no final do arquivo `~/.bashrc`
`alias sail='sh $([ -f sail ] && echo sail || echo vendor/bin/sail)`

## Primeira instalação
`docker run --rm \
    -u "$(id -u):$(id -g)" \
    -v "$(pwd):/var/www/html" \
    -w /var/www/html \
    laravelsail/php82-composer:latest \
    composer install --ignore-platform-reqs`

`cp .env.example .env`
`sail up`
### No segundo terminal
`sail artisan key:generate`

Aplicação estará disponível em http://localhost na máquina hospedeira

## Para desenvolver
`sail up`

## MongoDB Compass

`mongodb://root:password@localhost:27017/example?authSource=admin`
