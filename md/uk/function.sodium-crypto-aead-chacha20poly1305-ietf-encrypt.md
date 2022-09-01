---
navigation:
  - function.sodium-crypto-aead-chacha20poly1305-ietf-decrypt.html: « sodiumcryptoaeadchacha20poly1305ietfdecrypt
  - function.sodium-crypto-aead-chacha20poly1305-ietf-keygen.html: sodiumcryptoaeadchacha20poly1305ietfkeygen »
  - index.md: PHP Manual
  - ref.sodium.md: Функции Sodium
title: sodiumcryptoaeadchacha20poly1305ietfencrypt
---
# sodiumcryptoaeadchacha20poly1305ietfencrypt

(PHP 7> = 7.2.0, PHP 8)

sodiumcryptoaeadchacha20poly1305ietfencrypt — Зашифрувати повідомлення

### Опис

```methodsynopsis
sodium_crypto_aead_chacha20poly1305_ietf_encrypt(    string $message,    string $additional_data,    string $nonce,    string $key): string
```

Шифрує, а потім перевіряє справжність за допомогою ChaCha20-Poly1305 (варіант IETF).

Варіант IETF використовує 96-бітові одноразові номери та 32-бітові внутрішні лічильники замість 64-бітових і для того, і для іншого.

### Список параметрів

`message`

Текстове повідомлення, яке потрібно зашифрувати.

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 12 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає зашифрований текст та тег або **`false`** у разі виникнення помилки.
