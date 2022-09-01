---
navigation:
  - function.sodium-crypto-kdf-derive-from-key.html: « sodiumcryptokdfderivefromkey
  - function.sodium-crypto-kx-client-session-keys.html: sodiumcryptoкксclientsessionkeys »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumcryptokdfkeygen
---
# sodiumcryptokdfkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptokdfkeygen — Створює випадковий кореневий ключ для інтерфейсу KDF

### Опис

```methodsynopsis
sodium_crypto_kdf_keygen(): string
```

Створює випадковий ключ, що підходить для використання як кореневий ключ [sodiumcryptokdfderivefromkey()](function.sodium-crypto-kdf-derive-from-key.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Випадковий 256-бітний ключ.
