---
navigation:
  - function.sodium-crypto-stream-xchacha20.md: « sodium\_crypto\_stream\_xchacha20
  - function.sodium-crypto-stream.md: sodium\_crypto\_stream »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_stream\_xor
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_stream\_xor

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_stream\_xor — Шифрує повідомлення без автентифікації

### Опис

```methodsynopsis
sodium_crypto_stream_xor(string $message, string $nonce, string $key): string
```

Функція шифрує повідомлення за допомогою XSalsa20, але не надає жодної гарантії зашифрованого тексту для відкритого тексту.

### Список параметрів

`message`

Повідомлення для шифрування

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

Зашифровані повідомлення.
