---
navigation:
  - function.sodium-crypto-sign.md: « sodium\_crypto\_sign
  - function.sodium-crypto-stream-xchacha20-keygen.md: sodium\_crypto\_stream\_xchacha20\_keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_stream\_keygen
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_stream\_keygen

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_stream\_keygen - Генерує випадковий ключ sodium\_crypto\_stream

### Опис

```methodsynopsis
sodium_crypto_stream_keygen(): string
```

Створює ключ, який використовується в [sodium\_crypto\_stream()](function.sodium-crypto-stream.md) і [sodium\_crypto\_stream\_xor()](function.sodium-crypto-stream-xor.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ключ шифрування (256 біт).
