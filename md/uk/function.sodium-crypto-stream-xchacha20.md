---
navigation:
  - function.sodium-crypto-stream-xchacha20-xor.md: « sodium\_crypto\_stream\_xchacha20\_xor
  - function.sodium-crypto-stream-xor.md: sodium\_crypto\_stream\_xor »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_stream\_xchacha20
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_stream\_xchacha20

(PHP 8 >= 8.1.0)

sodium\_crypto\_stream\_xchacha20 — Розширює ключ та одноразовий номер у ключовий потік псевдовипадкових байтів

### Опис

```methodsynopsis
sodium_crypto_stream_xchacha20(int $length, string $nonce, string $key): string
```

Розширює ключ `key` та одноразовий номер `nonce` у ключовий потік псевдовипадкових байтів.

### Список параметрів

`length`

Бажана кількість байтів.

`nonce`

24-байтовий одноразовий номер.

`key`

Ключ, можливо, згенерований за допомогою функції [sodium\_crypto\_stream\_xchacha20\_keygen()](function.sodium-crypto-stream-xchacha20-keygen.md)

### Значення, що повертаються

Повертає псевдовипадковий потік, який можна використовувати функцією [sodium\_crypto\_stream\_xchacha20\_xor()](function.sodium-crypto-stream-xchacha20-xor.md)
