---
navigation:
  - function.openssl-private-decrypt.md: « openssl\_private\_decrypt
  - function.openssl-public-decrypt.md: openssl\_public\_decrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_private\_encrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_private\_encrypt

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_private\_encrypt - Шифрує дані секретним ключем

### Опис

```methodsynopsis
openssl_private_encrypt(    string $data,    string &$encrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $private_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**openssl\_private\_encrypt()** шифрує `data`с помощью секретного ключа`private_key`и сохраняет результат в`encrypted_data`. Далі можна розшифрувати за допомогою [openssl\_public\_decrypt()](function.openssl-public-decrypt.md)

Ця функція використовується, наприклад, для підпису даних. Щоб була впевненість у тому, хто саме надіслав повідомлення.

### Список параметрів

`data`

`encrypted_data`

`private_key`

`padding`

`padding` може бути однією з констант: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `private_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |

### Дивіться також

-   [openssl\_public\_encrypt()](function.openssl-public-encrypt.md) \- Шифрування даних відкритим ключем
-   [openssl\_public\_decrypt()](function.openssl-public-decrypt.md) \- Розшифрування даних за допомогою відкритого ключа
