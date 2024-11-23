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

## Lint

### ESLint

```
# チェック
$ docker compose exec react npm run lint

# 修正
$ docker compose exec react npm run lint:fix
```

### Prettier

```
# チェック
$ docker compose exec react npm run format

# 修正
$ docker compose exec react npm run format:fix
```

## アクセス

- フロントエンド： http://localhost:5173/
- バックエンド： http://localhost:3000/
