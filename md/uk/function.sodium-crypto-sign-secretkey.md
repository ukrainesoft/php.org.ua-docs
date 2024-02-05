---
navigation:
  - function.sodium-crypto-sign-publickey.md: « sodium\_crypto\_sign\_publickey
  - function.sodium-crypto-sign-seed-keypair.md: sodium\_crypto\_sign\_seed\_keypair »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_secretkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_secretkey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_secretkey — Витягує секретний ключ Ed25519 із пари ключів

### Опис

```methodsynopsis
sodium_crypto_sign_secretkey(string $key_pair): string
```

Витягує секретний ключ Ed25519 із пари ключів

### Список параметрів

`key_pair`

Ключевая пара Ed25519 (смотрите[sodium\_crypto\_sign\_keypair()](function.sodium-crypto-sign-keypair.md)) .

### Значення, що повертаються

Секретний ключ Ed25519
