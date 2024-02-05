---
navigation:
  - function.sodium-crypto-aead-aes256gcm-encrypt.md: « sodium\_crypto\_aead\_aes256gcm\_encrypt
  - function.sodium-crypto-aead-aes256gcm-keygen.md: sodium\_crypto\_aead\_aes256gcm\_keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_aead\_aes256gcm\_is\_available
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_aead\_aes256gcm\_is\_available

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_aead\_aes256gcm\_is\_available — Перевірити, чи підтримує обладнання AES256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_is_available(): bool
```

Значення цієї функції залежить від того, чи апаратне прискорення AES підтримує обладнання.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо шифрування за допомогою AES-256-GCM безпечне, інакше повертає **`false`**
