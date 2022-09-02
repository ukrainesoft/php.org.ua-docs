---
navigation:
  - function.openssl-private-encrypt.md: « opensslprivateencrypt
  - function.openssl-public-encrypt.md: opensslpublicencrypt »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpublicdecrypt
---
# opensslpublicdecrypt

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslpublicdecrypt — Розшифровування даних за допомогою відкритого ключа

### Опис

```methodsynopsis
openssl_public_decrypt(    string $data,    string &$decrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**opensslpublicdecrypt()** розшифровує дані `data`, які раніше були зашифровані за допомогою [opensslprivateencrypt()](function.openssl-private-encrypt.md) і зберігає результат у `decrypted_data`

Ви можете використовувати цю функцію, наприклад, щоб перевірити, чи було повідомлення написане власником закритого ключа.

### Список параметрів

`data`

`decrypted_data`

`public_key`

`public_key` повинен мати відповідний відкритий ключ.

`padding`

`padding` може бути однією з констант: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` або `OpenSSL X.509` |

### Дивіться також

-   [opensslprivateencrypt()](function.openssl-private-encrypt.md) - Шифрує дані секретним ключем
-   [opensslprivatedecrypt()](function.openssl-private-decrypt.md) - Розшифровує дані за допомогою закритого ключа
