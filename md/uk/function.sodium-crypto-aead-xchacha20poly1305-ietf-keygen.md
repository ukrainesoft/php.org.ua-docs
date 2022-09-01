---
navigation:
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.html: « sodiumcryptoaeadxchacha20poly1305ietfencrypt
  - function.sodium-crypto-auth-keygen.html: sodiumcryptoauthkeygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoaeadxchacha20poly1305ietfkeygen
---
# sodiumcryptoaeadxchacha20poly1305ietfkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadxchacha20poly1305ietfkeygen — Створює випадковий ключ XChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_xchacha20poly1305_ietf_keygen(): string
```

Створює випадковий ключ для використання в [sodiumcryptoaeadxchacha20poly1305ietfencrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.html) і [sodiumcryptoaeadxchacha20poly1305ietfdecrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-decrypt.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.
