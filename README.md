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
$ docker compose exec react npx eslint

# 修正
$ docker compose exec react npx eslint --fix
```

### Prettier

```
# チェック
$ docker compose exec react npx prettier . --check

# 修正
$ docker compose exec react npx prettier . --write
```

## アクセス

- フロントエンド： http://localhost:5173/
- バックエンド： http://localhost:3000/
