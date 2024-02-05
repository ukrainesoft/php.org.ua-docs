---
navigation:
  - function.openssl-x509-check-private-key.md: « openssl\_x509\_check\_private\_key
  - function.openssl-x509-export-to-file.md: openssl\_x509\_export\_to\_file »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_checkpurpose
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_checkpurpose

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_x509\_checkpurpose — Перевіряє, чи можна використовувати сертифікат для конкретних завдань

### Опис

```methodsynopsis
openssl_x509_checkpurpose(    OpenSSLCertificate|string $certificate,    int $purpose,    array $ca_info = [],    ?string $untrusted_certificates_file = null): bool|int
```

**openssl\_x509\_checkpurpose()** перевіряє сертифікат, щоб дізнатися, чи він може використовуватися із заданою метою `purpose`

### Список параметрів

`certificate`

Сертифікат

`purpose`

**Цілі **openssl\_x509\_checkpurpose()****

| Константа | Опис |
| --- | --- |
| X509\_PURPOSE\_SSL\_CLIENT | Чи можна використовувати сертифікат для з'єднання SSL на стороні клієнта? |
| X509\_PURPOSE\_SSL\_SERVER | Чи можна використовувати сертифікат для з'єднання SSL на стороні сервера? |
| X509\_PURPOSE\_NS\_SSL\_SERVER | Чи можна використовувати сервер Netscape SSL? |
| X509\_PURPOSE\_SMIME\_SIGN | Чи можна підписати S/MIME email? |
| X509\_PURPOSE\_SMIME\_ENCRYPT | Чи можна шифрувати S/MIME email? |
| X509\_PURPOSE\_CRL\_SIGN | Чи можна підписувати список відкликань сертифікатів (CRL)? |
| X509\_PURPOSE\_ANY | Чи можна використовувати будь-які завдання? |

Ці опції не є бінарною маскою – можна використовувати лише одне значення за раз!

`ca_info`

`ca_info` повинен містити масив довірених CA файлів/директорій, як описано на сторінці [перевірки сертифікатів](openssl.cert.verification.md)

`untrusted_certificates_file`

Якщо поставлено, то має містити шлях до PEM-файла, що містить сертифікати, які можуть бути використані для перевірки сертифіката, але не є довіреними.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо сертифікат можна використовувати за вказаним призначенням, **`false`** - якщо не можна і -1 у разі виникнення помилки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
| 8.0.0 | `untrusted_certificates_file` тепер допускає значення null. |
