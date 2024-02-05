---
navigation:
  - function.sodium-crypto-kx-keypair.md: « sodium\_crypto\_kx\_keypair
  - function.sodium-crypto-kx-secretkey.md: sodium\_crypto\_kx\_secretkey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_kx\_publickey
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_kx\_publickey

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_kx\_publickey — Витягує відкритий ключ із пари ключів crypto\_kx

### Опис

```methodsynopsis
sodium_crypto_kx_publickey(string $key_pair): string
```

Витягує відкритий ключ із пари ключів crypto\_kx.

### Список параметрів

`key_pair`

Пара ключей X25519, наПриклад, сгенерированная[sodium\_crypto\_kx\_keypair()](function.sodium-crypto-kx-keypair.md)

### Значення, що повертаються

Відкритий ключ X25519.
