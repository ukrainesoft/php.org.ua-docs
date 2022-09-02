---
navigation:
  - function.sodium-compare.md: « sodiumcompare
  - function.sodium-crypto-aead-aes256gcm-encrypt.md: sodiumcryptoaeadaes256gcmencrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoaeadaes256gcmdecrypt
---
# sodiumcryptoaeadaes256gcmdecrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadaes256gcmdecrypt — Перевірка та розшифрування повідомлення за допомогою AES-256-GCM

### Опис

```methodsynopsis
sodium_crypto_aead_aes256gcm_decrypt(    string $ciphertext,    string $additional_data,    string $nonce,    string $key): string|false
```

Перевіряє та розшифровує повідомлення за допомогою AES-256-GCM Доступно, лише якщо [sodiumcryptoaeadaes256gcmісavailable()](function.sodium-crypto-aead-aes256gcm-is-available.md) повертає **`true`**

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodiumcryptoaeadaes256gcmencrypt()](function.sodium-crypto-aead-aes256gcm-encrypt.md) (Зашифрований текст та тег, об'єднані).

`additional_data`

Додаткові перевірені дані. Це використовується для перевірки тега автентифікації, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 12 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає текст або **`false`** у разі виникнення помилки.
