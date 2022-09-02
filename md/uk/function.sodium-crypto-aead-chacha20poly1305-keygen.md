---
navigation:
  - function.sodium-crypto-aead-chacha20poly1305-ietf-keygen.md: « sodiumcryptoaeadchacha20poly1305ietfkeygen
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-decrypt.md: sodiumcryptoaeadxchacha20poly1305ietfdecrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoaeadchacha20poly1305keygen
---
# sodiumcryptoaeadchacha20poly1305keygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadchacha20poly1305keygen — Створює випадковий ключ ChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_chacha20poly1305_keygen(): string
```

Створює випадковий ключ для використання в [sodiumcryptoaeadchacha20poly1305encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.md) і [sodiumcryptoaeadchacha20poly1305decrypt()](function.sodium-crypto-aead-chacha20poly1305-decrypt.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.
