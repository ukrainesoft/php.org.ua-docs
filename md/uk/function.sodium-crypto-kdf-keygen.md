---
navigation:
  - function.sodium-crypto-kdf-derive-from-key.md: « sodium\_crypto\_kdf\_derive\_from\_key
  - function.sodium-crypto-kx-client-session-keys.md: sodium\_crypto\_kx\_client\_session\_keys »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_kdf\_keygen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_kdf\_keygen

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_kdf\_keygen — Створює випадковий кореневий ключ для інтерфейсу KDF

### Опис

```methodsynopsis
sodium_crypto_kdf_keygen(): string
```

Створює випадковий ключ, що підходить для використання як кореневий ключ [sodium\_crypto\_kdf\_derive\_from\_key()](function.sodium-crypto-kdf-derive-from-key.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Випадковий 256-бітний ключ.
