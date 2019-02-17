# Laravel_On_Docker
Laravel + Nginx + MySQL on Docker: Laravel dev without installing almost anything on your host except Docker!

## Further notes (Xueping Li)
### Based on:
- https://medium.com/@shakyShane/laravel-docker-part-1-setup-for-development-e3daaefaf3c

### Workflow:
``` 
Download  docker-compose.yml, web.dockerfile, app.dockerfile & edit if needed (like port mapping). Laravel 5.7.6 is included here. You may git clone any version from Laravel Github site. Note to run all the commands inside your app folder. 
```
* docker run --rm --interactive --tty --volume $PWD:/app composer install
* cp env.example .env
* docker-compose up
* docker-compose exec app php artisan key:generate
* docker-compose exec app php artisan optimize
``` 
open localhost:8000. Enjoy developing! 
```
