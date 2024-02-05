---
navigation:
  - function.sodium-crypto-box-keypair-from-secretkey-and-publickey.md: « sodium\_crypto\_box\_keypair\_from\_secretkey\_and\_publickey
  - function.sodium-crypto-box-open.md: sodium\_crypto\_box\_open »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_box\_keypair
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_box\_keypair

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_box\_keypair — Згенерувати випадковим чином секретний ключ та відповідний йому відкритий ключ

### Опис

```methodsynopsis
sodium_crypto_box_keypair(): string
```

Створює секретний та відкритий ключі як один рядок.

Щоб отримати секретний ключ із цього уніфікованого рядка ключової пари, дивіться [sodium\_crypto\_box\_secretkey()](function.sodium-crypto-box-secretkey.md). Щоб отримати відкритий ключ із цього уніфікованого рядка ключової пари, дивіться [sodium\_crypto\_box\_publickey()](function.sodium-crypto-box-publickey.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Один рядок містить секретний ключ X25519 і відповідний відкритий ключ X25519.
