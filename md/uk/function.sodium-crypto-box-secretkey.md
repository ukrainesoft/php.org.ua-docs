---
navigation:
  - function.sodium-crypto-box-seal.md: « sodium\_crypto\_box\_seal
  - function.sodium-crypto-box-seed-keypair.md: sodium\_crypto\_box\_seed\_keypair »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_secretkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_secretkey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_secretkey — Витягує секретний ключ із ключової пари crypto\_box

### Опис

```methodsynopsis
sodium_crypto_box_secretkey(string $key_pair): string
```

Отримує лише секретний ключ для цієї ключової пари.

### Список параметрів

`key_pair`

Пара ключей, созданная, например,[sodium\_crypto\_box\_keypair()](function.sodium-crypto-box-keypair.md) або [sodium\_crypto\_box\_seed\_keypair()](function.sodium-crypto-box-seed-keypair.md)

### Значення, що повертаються

Секретний ключ X25519.
