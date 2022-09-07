---
navigation:
  - function.sodium-crypto-sign-seed-keypair.md: « sodiumcryptosignseedkeypair
  - function.sodium-crypto-sign.md: sodiumcryptosign »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptosignverifydetached
---
# sodiumcryptosignverifydetached

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptosignverifydetached — Перевірити підпис для повідомлення

### Опис

```methodsynopsis
sodium_crypto_sign_verify_detached(string $signature, string $message, string $public_key): bool
```

Перевіряє підпис для повідомлення

### Список параметрів

`signature`

Криптографічний підпис, отриманий за допомогою [sodiumcryptosigndetached()](function.sodium-crypto-sign-detached.md)

`message`

Перевірене повідомлення

`public_key`

Відкритий ключ ed25519

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
