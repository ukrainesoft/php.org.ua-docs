---
navigation:
  - function.openssl-pkey-new.md: « openssl\_pkey\_new
  - function.openssl-private-encrypt.md: openssl\_private\_encrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_private\_decrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_private\_decrypt

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_private\_decrypt — Розшифровує дані за допомогою закритого ключа

### Опис

```methodsynopsis
openssl_private_decrypt(    string $data,    string &$decrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**openssl\_private\_decrypt()** розшифровує дані `data`, які раніше були зашифровані за допомогою [openssl\_public\_encrypt()](function.openssl-public-encrypt.md)и сохраняет результат в`decrypted_data`

Ви можете використовувати цю функцію, наприклад, для розшифровування даних, які повинні бути доступні тільки вам і більше.

### Список параметрів

`data`

`decrypted_data`

`private_key`

`private_key` має бути секретним ключем, що відповідає тому, чим ми шифрували дані.

`padding`

`padding` може приймати одне з наступних значень: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_SSLV23_PADDING`** **`OPENSSL_PKCS1_OAEP_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |

### Дивіться також

-   [openssl\_public\_encrypt()](function.openssl-public-encrypt.md) \- Шифрування даних відкритим ключем
-   [openssl\_public\_decrypt()](function.openssl-public-decrypt.md) \- Розшифрування даних за допомогою відкритого ключа
