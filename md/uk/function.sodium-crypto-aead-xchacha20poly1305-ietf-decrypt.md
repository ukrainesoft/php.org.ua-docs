---
navigation:
  - function.sodium-crypto-aead-chacha20poly1305-keygen.md: « sodium\_crypto\_aead\_chacha20poly1305\_keygen
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-encrypt.md: sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt — (Переважно) Перевіряє, потім розшифровує за допомогою XChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_xchacha20poly1305_ietf_decrypt(    string $ciphertext,    string $additional_data,    string $nonce,    string $key): string|false
```

(Переважно) Перевіряє, потім розшифровує за допомогою XChaCha20-Poly1305

Як правило, XChaCha20-Poly1305 – найкращий з наявних режимів AEAD для використання.

### Список параметрів

`ciphertext`

Має бути у форматі, наданому [sodium\_crypto\_aead\_chacha20poly1305\_ietf\_encrypt()](function.sodium-crypto-aead-chacha20poly1305-ietf-encrypt.md) (Зашифрований текст та тег, об'єднані).

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає текст або \*\*`false`\*\*в случае возникновения ошибки.
