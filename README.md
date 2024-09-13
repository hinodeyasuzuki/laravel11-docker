## create

```
docker compose up -d
```

- ./src/pulic : web root folder out of container. 
- /var/www : bash root of php container.
- /var/www/html : web access root of php container.

create ./src/public/index.html file and access
```
http://localhost:8000
```

phpMyAdmin
```
http://localhost:4040
```
in case of session error

```
docker compose exec php bash
chmod 777 -R html/phpmyadmin
```


## install laravel

```
docker compose exec php bash
cd html
composer create-project laravel/laravel src
chmod 777 -R src
cd src
vi .env
```

.env fix
```
DB_CONNECTION=mysql
DB_PORT=3306
DB_HOST=db
DB_DATABASE=database
DB_USERNAME=db-user
DB_PASSWORD=db-pass
```

DB create
```
php artisan migrate
```


