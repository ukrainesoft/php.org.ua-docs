---
navigation:
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-keygen.md: « sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen
  - function.sodium-crypto-auth-verify.md: sodium\_crypto\_auth\_verify »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_auth\_keygen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_auth\_keygen

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_auth\_keygen — Створює випадковий ключ для sodium\_crypto\_auth

### Опис

```methodsynopsis
sodium_crypto_auth_keygen(): string
```

Створює ключ для використання в [sodium\_crypto\_auth()](function.sodium-crypto-auth.md) і [sodium\_crypto\_auth\_verify()](function.sodium-crypto-auth-verify.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає 256-бітний випадковий ключ.
