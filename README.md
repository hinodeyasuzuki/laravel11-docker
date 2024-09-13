## 概要

./src/pulic がwebのルートフォルダになる。
```
http://localhost:8000
```

## laravelの場合のインストール

```
docker compose exec php bash
composer create-project laravel/laravel src
cd src
vi .env
```

（.envのDBの設定）
```
DB_CONNECTION=mysql
DB_PORT=3306
DB_HOST=db
DB_DATABASE=database
DB_USERNAME=db-user
DB_PASSWORD=db-pass
```

DB作成
```
php artisan migrate
```


