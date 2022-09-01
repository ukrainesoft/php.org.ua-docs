---
navigation:
  - function.sodium-crypto-stream-xor.html: « sodiumcryptostreamxor
  - function.sodium-hex2bin.html: sodiumhex2bin »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptostream
---
# sodiumcryptostream

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptostream - Створює детерміновану послідовність байтів з початкового числа

### Опис

```methodsynopsis
sodium_crypto_stream(int $length, string $nonce, string $key): string
```

Створює детерміновану послідовність байтів із початкового числа з використанням потокового шифру XSalsa20.

### Список параметрів

`length`

Кількість байтів, що повертаються.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Рядок псевдовипадкових байтів.
