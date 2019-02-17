# Laravel_On_Docker
Laravel + Nginx + MySQL on Docker 

## Further notes (Xueping Li)
Based on:
- https://medium.com/@shakyShane/laravel-docker-part-1-setup-for-development-e3daaefaf3c

Workflow:

* cd
* mkdir xp1site ### your site name
* cd xp1site
* git clone LARAVEL_GIT_URL
* rm -rf .git
* docker run --rm -v $(pwd):/app composer/composer install
``` prepare docker-compose.yml, web.dockerfile, app.dockerfile
* cp .env.example .env
* docker-compose up
* docker-compose exec app php artisan key:generate
* docker-compose exec app php artisan optimize
``` open localhost:8000. Enjoy developing!
