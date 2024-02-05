---
navigation:
  - function.openssl-x509-parse.md: « openssl\_x509\_parse
  - function.openssl-x509-verify.md: openssl\_x509\_verify »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_read
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_read

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_x509\_read — Розібрати сертифікат X.509 та повернути для нього об'єкт

### Опис

```methodsynopsis
openssl_x509_read(OpenSSLCertificate|string $certificate): OpenSSLCertificate|false
```

\*\*openssl\_x509\_read()\*\*извлекает сертификат из`certificate` та повертає об'єкт [OpenSSLCertificate](class.opensslcertificate.md)для него.

### Список параметрів

`certificate`

Сертифікат X509 Список коректних значень дивіться на сторінці [Параметри ключів та сертифікатів](openssl.certparams.md)

### Значення, що повертаються

Повертає об'єкт [OpenSSLCertificate](class.opensslcertificate.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | У разі успішного виконання повертає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше повертався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
