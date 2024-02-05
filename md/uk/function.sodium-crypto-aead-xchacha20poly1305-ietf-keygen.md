---
navigation:
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.md: « sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt
  - function.sodium-crypto-auth-keygen.md: sodium\_crypto\_auth\_keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen — Створює випадковий ключ XChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_xchacha20poly1305_ietf_keygen(): string
```

Створює випадковий ключ для використання в [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.md) і [sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt()](function.sodium-crypto-aead-xchacha20poly1305-ietf-decrypt.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.
