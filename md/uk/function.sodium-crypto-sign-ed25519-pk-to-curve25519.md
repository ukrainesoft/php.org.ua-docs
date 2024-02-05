---
navigation:
  - function.sodium-crypto-sign-detached.md: « sodium\_crypto\_sign\_detached
  - function.sodium-crypto-sign-ed25519-sk-to-curve25519.md: sodium\_crypto\_sign\_ed25519\_sk\_to\_curve25519 »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_sign\_ed25519\_pk\_to\_curve25519 — Перетворення відкритого ключа системи Ed25519 на відкритий ключ Curve25519

### Опис

```methodsynopsis
sodium_crypto_sign_ed25519_pk_to_curve25519(string $public_key): string
```

Обчислює біраціонально-еквівалентний відкритий ключ X25519 для відкритого ключа Ed25519.

### Список параметрів

`public_key`

Відкритий ключ, що підходить для функцій crypto\_sign.

### Значення, що повертаються

Відкритий ключ, що підходить для функцій crypto\_box.
