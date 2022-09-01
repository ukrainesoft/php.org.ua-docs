---
navigation:
  - function.sodium-crypto-aead-chacha20poly1305-decrypt.html: « sodiumcryptoaeadchacha20poly1305decrypt
  - function.sodium-crypto-aead-chacha20poly1305-ietf-decrypt.html: sodiumcryptoaeadchacha20poly1305ietfdecrypt »
  - index.html: PHP Manual
  - ref.sodium.html: Функции Sodium
title: sodiumcryptoaeadchacha20poly1305encrypt
---
# sodiumcryptoaeadchacha20poly1305encrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadchacha20poly1305encrypt — Шифрує, а потім перевіряє справжність за допомогою ChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_chacha20poly1305_encrypt(    string $message,    string $additional_data,    string $nonce,    string $key): string
```

Шифрує, а потім перевіряє справжність за допомогою ChaCha20-Poly1305

### Список параметрів

`message`

Текстове повідомлення, яке потрібно зашифрувати.

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 8 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає зашифрований текст та тег або **`false`** у разі виникнення помилки.
