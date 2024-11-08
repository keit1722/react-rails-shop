# react-rails-shop

## 環境構築

### インストール

```
$ docker compose build --no-cache
$ docker compose run --rm rails bundle install
$ docker compose up
```

### DB のセットアップ

```
$ docker compose run --rm rails bundle exec rails db:create
$ docker compose run --rm rails bundle exec rails db:migrate
```
