---
navigation:
  - function.sodium-crypto-kx-publickey.md: « sodium\_crypto\_kx\_publickey
  - function.sodium-crypto-kx-seed-keypair.md: sodium\_crypto\_kx\_seed\_keypair »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_kx\_secretkey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_kx\_secretkey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_kx\_secretkey — Витягує секретний ключ із пари ключів crypto\_kx

### Опис

```methodsynopsis
sodium_crypto_kx_secretkey(string $key_pair): string
```

Витягує секретний ключ із пари ключів crypto\_kx.

### Список параметрів

`key_pair`

Пара ключей X25519, наПриклад, сгенерированная[sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.md)

### Значення, що повертаються

Секретний ключ X25519.
