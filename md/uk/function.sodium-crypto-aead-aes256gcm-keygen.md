---
navigation:
  - function.sodium-crypto-aead-aes256gcm-is-available.md: « sodium\_crypto\_aead\_aes256gcm\_is\_available
  - function.sodium-crypto-aead-chacha20poly1305-decrypt.md: sodium\_crypto\_aead\_chacha20poly1305\_decrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_aead\_aes256gcm\_keygen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_aead\_aes256gcm\_keygen

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_aead\_aes256gcm\_keygen — Створює випадковий ключ AES-256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_keygen(): string
```

Створює випадковий ключ для використання в [sodium\_crypto\_aead\_aes256gcm\_encrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.md) і [sodium\_crypto\_aead\_aes256gcm\_decrypt()](function.sodium-crypto-aead-aes256gcm-decrypt.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.
