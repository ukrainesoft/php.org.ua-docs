---
navigation:
  - function.sodium-crypto-stream-xchacha20-xor.html: « sodiumcryptostreamxchacha20xor
  - function.sodium-crypto-stream-xor.html: sodiumcryptostreamxor »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptostreamxchacha20
---
# sodiumcryptostreamxchacha20

(PHP 8> = 8.1.0)

sodiumcryptostreamxchacha20 — Розширює ключ та одноразовий номер у ключовий потік псевдовипадкових байтів

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

Ключ, можливо, згенерований за допомогою функції [sodiumcryptostreamxchacha20keygen()](function.sodium-crypto-stream-xchacha20-keygen.md)

### Значення, що повертаються

Повертає псевдовипадковий потік, який можна використовувати функцією [sodiumcryptostreamxchacha20xor()](function.sodium-crypto-stream-xchacha20-xor.md)
