---
navigation:
  - function.sodium-crypto-aead-chacha20poly1305-keygen.html: « sodiumcryptoaeadchacha20poly1305keygen
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.html: sodiumcryptoaeadxchacha20poly1305ietfencrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoaeadxchacha20poly1305ietfdecrypt
---
# sodiumcryptoaeadxchacha20poly1305ietfdecrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadxchacha20poly1305ietfdecrypt — (Переважно) Перевіряє, потім розшифровує за допомогою XChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_xchacha20poly1305_ietf_decrypt(    string $ciphertext,    string $additional_data,    string $nonce,    string $key): string|false
```

(Переважно) Перевіряє, потім розшифровує за допомогою XChaCha20-Poly1305

Як правило, XChaCha20-Poly1305 – найкращий з наявних режимів AEAD для використання.

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodiumcryptoaeadchacha20poly1305ietfencrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.md) (Зашифрований текст та тег, об'єднані).

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [randombytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає текст або **`false`** у разі виникнення помилки.
