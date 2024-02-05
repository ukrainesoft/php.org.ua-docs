---
navigation:
  - function.sodium-crypto-box-publickey-from-secretkey.md: « sodium\_crypto\_box\_publickey\_from\_secretkey
  - function.sodium-crypto-box-seal-open.md: sodium\_crypto\_box\_seal\_open »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_publickey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_publickey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_publickey — Витягує відкритий ключ із ключової пари crypto\_box

### Опис

```methodsynopsis
sodium_crypto_box_publickey(string $key_pair): string
```

Отримує лише відкритий ключ із ключової пари.

### Список параметрів

`key_pair`

Ключевая пара, созданная, например,[sodium\_crypto\_box\_keypair()](function.sodium-crypto-box-keypair.md) або [sodium\_crypto\_box\_seed\_keypair()](function.sodium-crypto-box-seed-keypair.md)

### Значення, що повертаються

Відкритий ключ X25519.
