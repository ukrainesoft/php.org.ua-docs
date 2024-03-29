---
navigation:
  - function.openssl-public-decrypt.md: « openssl\_public\_decrypt
  - function.openssl-random-pseudo-bytes.md: openssl\_random\_pseudo\_bytes »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_public\_encrypt
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_public\_encrypt

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_public\_encrypt — Шифрування даних відкритим ключем

### Опис

```methodsynopsis
openssl_public_encrypt(    string $data,    string &$encrypted_data,    OpenSSLAsymmetricKey|OpenSSLCertificate|array|string $public_key,    int $padding = OPENSSL_PKCS1_PADDING): bool
```

**openssl\_public\_encrypt()** шифрує `data` відкритим ключем `public_key` і зберігає в `encrypted_data`. Згодом розшифрувати їх можна функцією [openssl\_private\_decrypt()](function.openssl-private-decrypt.md)

Ця функція використовується, наприклад, для надсилання повідомлень, які може прочитати тільки власник закритого ключа і ніхто більше. Також її можна використовуватиме шифрування інформації у базі даних.

### Список параметрів

`data`

`encrypted_data`

Міститиме результат шифрування.

`public_key`

Відкритий ключ.

`padding`

`padding` може бути однією з констант: **`OPENSSL_PKCS1_PADDING`** **`OPENSSL_SSLV23_PADDING`** **`OPENSSL_PKCS1_OAEP_PADDING`** **`OPENSSL_NO_PADDING`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `public_key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md) або [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key`или`OpenSSL X.509` |

### Дивіться також

-   [openssl\_private\_encrypt()](function.openssl-private-encrypt.md) \- Шифрує дані секретним ключем
-   [openssl\_private\_decrypt()](function.openssl-private-decrypt.md) \- Розшифровує дані за допомогою закритого ключа
