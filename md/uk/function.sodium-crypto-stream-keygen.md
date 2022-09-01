---
navigation:
  - function.sodium-crypto-sign.html: « sodiumcryptosign
  - function.sodium-crypto-stream-xchacha20-keygen.html: sodiumcryptostreamxchacha20keygen »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumcryptostreamkeygen
---
# sodiumcryptostreamkeygen

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptostreamkeygen - Генерує випадковий ключ sodiumcryptostream

### Опис

```methodsynopsis
sodium_crypto_stream_keygen(): string
```

Створює ключ, який використовується в [sodiumcryptostream()](function.sodium-crypto-stream.html) і [sodiumcryptostreamxor()](function.sodium-crypto-stream-xor.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ шифрування (256 біт).
