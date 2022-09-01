---
navigation:
  - function.sodium-crypto-sign-detached.html: « sodiumcryptosigndetached
  - function.sodium-crypto-sign-ed25519-sk-to-curve25519.html: sodiumcryptosigned25519сктоcurve25519 »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumcryptosigned25519пктоcurve25519
---
# sodiumcryptosigned25519пктоcurve25519

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosigned25519пктоcurve25519 — Перетворення відкритого ключа системи Ed25519 на відкритий ключ Curve25519

### Опис

```methodsynopsis
sodium_crypto_sign_ed25519_pk_to_curve25519(string $public_key): string
```

Обчислює біраціонально-еквівалентний відкритий ключ X25519 для відкритого ключа Ed25519.

### Список параметрів

`public_key`

Відкритий ключ, що підходить для функцій cryptosign.

### Значення, що повертаються

Відкритий ключ, що підходить для функцій cryptobox.
