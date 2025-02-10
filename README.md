## Primeira utilização do Laravel
Adicone esta linha no final do arquivo `~/.bashrc`
`alias sail='sh $([ -f sail ] && echo sail || echo vendor/bin/sail)`

## Primeira instalação
`cp .env.example .env`
`mkdir -p storage/framework/{cache,sessions,views} && mkdir -p storage/logs`
<!-- `sudo chmod o+w ./storage/ -R` -->
`docker compose up --build`
### No segundo terminal
`docker exec -it example-app-mongo-laravel.test-1 composer install`
### Volte ao primeiro terminal e mate o processo 
CTRL + C
`./vendor/bin/sail up`
### No segundo terminal
`./vendor/bin/sail artisan key:generate`

## Para desenvolver
`sail up`
