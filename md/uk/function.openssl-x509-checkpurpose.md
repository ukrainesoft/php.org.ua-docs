---
navigation:
  - function.openssl-x509-check-private-key.md: « opensslx509checkprivatekey
  - function.openssl-x509-export-to-file.md: opensslx509exportтоfile »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslx509checkpurpose
---
# opensslx509checkpurpose

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslx509checkpurpose — Перевіряє, чи можна використовувати сертифікат для конкретних завдань

### Опис

```methodsynopsis
openssl_x509_checkpurpose(    OpenSSLCertificate|string $certificate,    int $purpose,    array $ca_info = [],    ?string $untrusted_certificates_file = null): bool|int
```

**opensslx509checkpurpose()** перевіряє сертифікат, щоб дізнатися, чи він може використовуватися із заданою метою `purpose`

### Список параметрів

`certificate`

Сертифікат

`purpose`

**Цілі **opensslx509checkpurpose()****

| Константа | Описание |
| --- | --- |
| X509PURPOSESSLCLIENT | Чи можна використовувати сертифікат для з'єднання SSL на стороні клієнта? |
| X509PURPOSESSLSERVER | Чи можна використовувати сертифікат для з'єднання SSL на стороні сервера? |
| X509PURPOSEНСSSLSERVER | Чи можна використовувати сервер Netscape SSL? |
| X509PURPOSESMIMESIGN | Чи можна підписати S/MIME email? |
| X509PURPOSESMIMEENCRYPT | Чи можна шифрувати S/MIME email? |
| X509PURPOSECRLSIGN | Чи можна підписувати список відкликань сертифікатів (CRL)? |
| X509PURPOSEANY | Чи можна використовувати будь-які завдання? |

Ці опції не є бінарною маскою – можна використовувати лише одне значення за раз!

`ca_info`

`ca_info` повинен містити масив довірених CA файлів/директорій, як описано на сторінці [проверки сертификатов](openssl.cert.verification.md)

`untrusted_certificates_file`

Якщо задано, то має містити шлях до PEM-файлу, що містить сертифікати, які можуть бути використані для перевірки сертифіката, але не є довіреними.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо сертифікат можна використовувати за вказаним призначенням, **`false`** - якщо не можна і -1 у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509` |
|  | `untrusted_certificates_file` тепер допускає значення null. |
