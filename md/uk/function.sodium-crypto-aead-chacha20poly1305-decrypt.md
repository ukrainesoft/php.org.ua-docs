---
navigation:
  - function.sodium-crypto-aead-aes256gcm-keygen.md: « sodiumcryptoaeadaes256gcmkeygen
  - function.sodium-crypto-aead-chacha20poly1305-encrypt.md: sodiumcryptoaeadchacha20poly1305encrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoaeadchacha20poly1305decrypt
---
# sodiumcryptoaeadchacha20poly1305decrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadchacha20poly1305decrypt — Перевіряє, потім розшифровує за допомогою ChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_chacha20poly1305_decrypt(    string $ciphertext,    string $additional_data,    string $nonce,    string $key): string|false
```

Перевіряє, потім розшифровує за допомогою ChaCha20-Poly1305

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodiumcryptoaeadchacha20poly1305encrypt()](function.sodium-crypto-aead-chacha20poly1305-encrypt.md) (Зашифрований текст та тег, об'єднані).

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 8 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає текст або **`false`** у разі виникнення помилки.
