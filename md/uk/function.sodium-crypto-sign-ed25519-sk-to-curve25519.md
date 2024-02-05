---
navigation:
  - function.sodium-crypto-sign-ed25519-pk-to-curve25519.md: « sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519
  - function.sodium-crypto-sign-keypair-from-secretkey-and-publickey.md: sodium\_crypto\_sign\_keypair\_from\_secretkey\_and\_publickey »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519 — Перетворити секретний ключ із системи Ed25519 на секретний ключ Curve25519

### Опис

```methodsynopsis
sodium_crypto_sign_ed25519_sk_to_curve25519(string $secret_key): string
```

Обчислює біраціонально-еквівалентний секретний ключ X25519 для секретного ключа Ed25519.

### Список параметрів

`secret_key`

Секретний ключ, що підходить для функцій crypto\_sign.

### Значення, що повертаються

Секретний ключ, що підходить для функцій crypto\_box.
