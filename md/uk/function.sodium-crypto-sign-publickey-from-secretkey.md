---
navigation:
  - function.sodium-crypto-sign-open.md: « sodium\_crypto\_sign\_open
  - function.sodium-crypto-sign-publickey.md: sodium\_crypto\_sign\_publickey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_publickey\_from\_secretkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_publickey\_from\_secretkey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_publickey\_from\_secretkey — Витягує відкритий ключ Ed25519 із секретного ключа

### Опис

```methodsynopsis
sodium_crypto_sign_publickey_from_secretkey(string $secret_key): string
```

Витягує відкритий ключ Ed25519 із секретного ключа

### Список параметрів

`secret_key`

Секретний ключ Ed25519

### Значення, що повертаються

Відкритий ключ Ed25519
