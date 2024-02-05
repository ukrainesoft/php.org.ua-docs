---
navigation:
  - function.sodium-crypto-stream-xor.md: « sodium\_crypto\_stream\_xor
  - function.sodium-hex2bin.md: sodium\_hex2bin »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_stream
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_stream

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_stream - Створює детерміновану послідовність байтів з початкового числа

### Опис

```methodsynopsis
sodium_crypto_stream(int $length, string $nonce, string $key): string
```

Створює детерміновану послідовність байтів із початкового числа з використанням потокового шифру XSalsa20.

### Список параметрів

`length`

Кількість байтів, що повертаються.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Рядок псевдовипадкових байтів.
