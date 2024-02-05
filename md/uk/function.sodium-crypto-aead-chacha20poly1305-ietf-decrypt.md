---
navigation:
  - function.sodium-crypto-aead-chacha20poly1305-encrypt.md: « sodium\_crypto\_aead\_chacha20poly1305\_encrypt
  - function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.md: sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_aead\_chacha20poly1305\_ietf\_decrypt — Перевірити, чи зашифрований текст містить допустимий тег

### Опис

```methodsynopsis
sodium_crypto_aead_chacha20poly1305_ietf_decrypt(    string $ciphertext,    string $additional_data,    string $nonce,    string $key): string|false
```

Перевіряє, потім розшифровує ChaCha20-Poly1305 (варіант IETF).

Варіант IETF використовує 96-бітові одноразові номери та 32-бітові внутрішні лічильники замість 64-бітових і для того, і для іншого.

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.md) (Зашифрований текст та тег, об'єднані).

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 12 байт.

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає текст або \*\*`false`\*\*в случае возникновения ошибки.
