# 二重プロキシ動作テスト

## 実行方法

```bash
docker compose up -d
docker compose exec target curl -I https://www.google.com
docker compose logs proxy-b
```

## 概要



## 既知の問題

- リバースプロキシ(proxy-a)が構築できていない
  - このため、targetのhttps_proxyはproxy-bを向いている
- ログのタイムゾーンがJSTにならない
- 構築中のため、squid.confをbind mountしている
