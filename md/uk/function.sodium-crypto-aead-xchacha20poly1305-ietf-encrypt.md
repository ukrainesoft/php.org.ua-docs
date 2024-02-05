---
navigation:
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-decrypt.md: « sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_decrypt
  - function.sodium-crypto-aead-xchacha20poly1305-ietf-keygen.md: sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_keygen »
  - index.md: PHP Manual
  - ref.sodium.md: Опції Sodium
title: sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt

(PHP 7 >= 7.2.0, PHP 8)

sodium\_crypto\_aead\_xchacha20poly1305\_ietf\_encrypt — (Переважно) Шифрує, а потім перевіряє справжність за допомогою XChaCha20-Poly1305

### Опис

```methodsynopsis
sodium_crypto_aead_xchacha20poly1305_ietf_encrypt(    string $message,    string $additional_data,    string $nonce,    string $key): string
```

Шифрує, а потім перевіряє справжність за допомогою XChaCha20-Poly1305 (варіант eXtended-nonce).

Як правило, XChaCha20-Poly1305 – найкращий з наявних режимів AEAD для використання.

### Список параметрів

`message`

Текстове повідомлення, яке потрібно зашифрувати.

`additional_data`

Додаткові перевірені дані. Це використовується при перевірці автентичності, доданого до зашифрованого тексту, але він не шифрується і не зберігається в зашифрованому тексті.

`nonce`

Номер, який потрібно використовувати лише один раз для кожного повідомлення. Довжина 24 байти. Це досить велика межа для випадкової генерації (наприклад, [random\_bytes()](function.random-bytes.md)

`key`

Ключ шифрування (256 біт).

### Значення, що повертаються

У разі успішного виконання повертає зашифрований текст та тег або \*\*`false`\*\*в случае возникновения ошибки.
