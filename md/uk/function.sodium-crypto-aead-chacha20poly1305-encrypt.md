---
navigation:
  - function.sodium-crypto-aead-chacha20poly1305-decrypt.md: « sodium\_crypto\_aead\_chacha20poly1305\_decrypt
  - function.sodium-crypto-aead-chacha20poly1305-ietf-decrypt.md: sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_aead\_chacha20poly1305\_encrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_aead\_chacha20poly1305\_encrypt

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_aead\_chacha20poly1305\_encrypt — Шифрує, а потім перевіряє справжність за допомогою ChaCha20-Poly1305

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

У разі успішного виконання повертає зашифрований текст та тег або \*\*`false`\*\*в случае возникновения ошибки.
