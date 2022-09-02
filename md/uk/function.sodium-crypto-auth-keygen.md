---
navigation:
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-keygen.md: « sodiumcryptoaeadxchacha20poly1305ietfkeygen
  - function.sodium-crypto-auth-verify.md: sodiumcryptoauthverify »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoauthkeygen
---
# sodiumcryptoauthkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoauthkeygen — Створює випадковий ключ для sodiumcryptoauth

### Опис

```methodsynopsis
sodium_crypto_auth_keygen(): string
```

Створює ключ для використання в [sodiumcryptoauth()](function.sodium-crypto-auth.md) і [sodiumcryptoauthverify()](function.sodium-crypto-auth-verify.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.
