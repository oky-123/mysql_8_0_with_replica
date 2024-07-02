# このリポジトリについて

DockerでMySQL8.0のレプリケーション環境を構築するためのリポジトリです。

下記のポートでMySQLが起動します。

- primary → `3307`
- replica → `3308`

## 起動方法

```sh
docker compose up
```

クライアントの接続↓

```sh
# プライマリへの接続
docker exec -it mysql_primary mysql -uroot -ppassword

# レプリカへの接続
docker exec -it mysql_replica mysql -uroot -ppassword
```

## 対応していないこと

- ユーザーの作成 ... 現状デフォルトで作成されるrootユーザーのみで動かしています。
