---
navigation:
  - function.openssl-private-encrypt.md: « openssl\_private\_encrypt
  - function.openssl-public-encrypt.md: openssl\_public\_encrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_public\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_public\_decrypt

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_public\_decrypt — Розшифровування даних за допомогою відкритого ключа

### Опис

```methodsynopsis
openssl_public_decrypt(    string $data,    string &$decrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**openssl\_public\_decrypt()** розшифровує дані `data`, які раніше були зашифровані за допомогою [openssl\_private\_encrypt()](function.openssl-private-encrypt.md)и сохраняет результат в`decrypted_data`

Ви можете використовувати цю функцію, наприклад, щоб перевірити, чи було повідомлення написане власником закритого ключа.

### Список параметрів

`data`

`decrypted_data`

`public_key`

`public_key` повинен мати відповідний відкритий ключ.

`padding`

`padding` може бути однією з констант: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |

### Дивіться також

-   [openssl\_private\_encrypt()](function.openssl-private-encrypt.md) \- Шифрує дані секретним ключем
-   [openssl\_private\_decrypt()](function.openssl-private-decrypt.md) \- Розшифровує дані за допомогою закритого ключа
