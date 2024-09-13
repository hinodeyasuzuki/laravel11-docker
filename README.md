## create

```
docker compose up -d
```

./src/pulic is web root folder. You need to create.
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
chmod 777 -R phpmyadmin
```


## install laravel


```
docker compose exec php bash
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


