---
navigation:
  - function.openssl-pkcs7-sign.md: « openssl\_pkcs7\_sign
  - function.openssl-pkey-derive.md: openssl\_pkey\_derive »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkcs7\_verify
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkcs7\_verify

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_pkcs7\_verify — Перевірити підпис повідомлення S/MIME

### Опис

```methodsynopsis
openssl_pkcs7_verify(    string $input_filename,    int $flags,    ?string $signers_certificates_filename = null,    array $ca_info = [],    ?string $untrusted_certificates_filename = null,    ?string $content = null,    ?string $output_filename = null): bool|int
```

**openssl\_pkcs7\_verify()** читає S/MIME повідомлення з файлу та перевіряє його підпис.

### Список параметрів

`input_filename`

Шлях до файлу із повідомленням.

`flags`

`flags` можна використовувати модифікації процесу перевірки. Детальніше дивіться [константи PKCS7](openssl.pkcs7.flags.md)

`signers_certificates_filename`

Если задан параметр`signers_certificates_filename`, то в ньому має бути рядок з ім'ям файлу, в який буде збережено сертифікати, використані під час підписання, у форматі PEM.

`ca_info`

Если задан параметр`ca_info`, то в ньому повинна бути інформація про довірені сертифікати CA, які необхідно використовувати в процесі перевірки. Докладніше читайте на сторінці [перевірки сертифікатів](openssl.cert.verification.md)

`untrusted_certificates_filename`

Если задан параметр`untrusted_certificates_filename`, у ньому має бути ім'я файлу, що містить набір недовірених сертифікатів CA.

`content`

В параметре`content` можна вказати ім'я файлу, до якого буде записано верифіковані дані без інформації про підпис.

`output_filename`

### Значення, що повертаються

Повертає **`true`**, якщо перевірка успішна, \*\*`false`\*\*якщо немає і -1 у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `signers_certificates_filename` `untrusted_certificates_filename` `content`и`output_filename` тепер допускають значення null. |
| 7.2.0 | Добавлен параметр`output_filename` |

### Примітки

> **Зауваження**: Как указано в RFC 2045, длина параметра`input_filename` не повинна бути довшою за 76 символів.
