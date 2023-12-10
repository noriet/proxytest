# 多段プロキシ動作テスト

## 実行方法

```bash
docker compose up -d
docker compose exec target curl -I https://www.google.com
docker compose logs
```

## 概要


## 既知の問題

- ログのタイムゾーンがJSTにならない
