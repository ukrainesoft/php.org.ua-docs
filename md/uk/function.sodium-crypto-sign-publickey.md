---
navigation:
  - function.sodium-crypto-sign-publickey-from-secretkey.md: « sodium\_crypto\_sign\_publickey\_from\_secretkey
  - function.sodium-crypto-sign-secretkey.md: sodium\_crypto\_sign\_secretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_publickey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_publickey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_publickey — Витягує відкритий ключ Ed25519 із пари ключів

### Опис

```methodsynopsis
sodium_crypto_sign_publickey(string $key_pair): string
```

Витягує відкритий ключ Ed25519 із пари ключів.

### Список параметрів

`key_pair`

Ключевая пара Ed25519 (смотрите[sodium\_crypto\_sign\_keypair()](function.sodium-crypto-sign-keypair.md)) .

### Значення, що повертаються

Відкритий ключ Ed25519
