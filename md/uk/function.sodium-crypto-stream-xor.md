---
navigation:
  - function.sodium-crypto-stream-xchacha20.html: « sodiumcryptostreamxchacha20
  - function.sodium-crypto-stream.html: sodiumcryptostream »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptostreamxor
---
# sodiumcryptostreamxor

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptostreamxor — Шифрує повідомлення без автентифікації

### Опис

```methodsynopsis
sodium_crypto_stream_xor(string $message, string $nonce, string $key): string
```

Функція шифрує повідомлення за допомогою XSalsa20, але не надає жодної гарантії зашифрованого тексту для відкритого тексту.

### Список параметрів

`message`

Повідомлення для шифрування

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Зашифровані повідомлення.
