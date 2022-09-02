---
navigation:
  - function.sodium-crypto-sign.md: « sodiumcryptosign
  - function.sodium-crypto-stream-xchacha20-keygen.md: sodiumcryptostreamxchacha20keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptostreamkeygen
---
# sodiumcryptostreamkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptostreamkeygen - Генерує випадковий ключ sodiumcryptostream

### Опис

```methodsynopsis
sodium_crypto_stream_keygen(): string
```

Створює ключ, який використовується в [sodiumcryptostream()](function.sodium-crypto-stream.md) і [sodiumcryptostreamxor()](function.sodium-crypto-stream-xor.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ шифрування (256 біт).
