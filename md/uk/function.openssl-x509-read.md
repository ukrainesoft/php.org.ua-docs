---
navigation:
  - function.openssl-x509-parse.md: « opensslx509parse
  - function.openssl-x509-verify.md: opensslx509verify »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslx509read
---
# opensslx509read

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslx509read — Розібрати сертифікат X.509 та повернути для нього об'єкт

### Опис

```methodsynopsis
openssl_x509_read(OpenSSLCertificate|string $certificate): OpenSSLCertificate|false
```

**opensslx509read()** отримує сертифікат з `certificate` та повертає об'єкт [OpenSSLCertificate](class.opensslcertificate.md) для нього.

### Список параметрів

`certificate`

Сертифікат X509 Список коректних значень дивіться на сторінці [Параметри ключів та сертифікатів](openssl.certparams.md)

### Значення, що повертаються

Повертає об'єкт [OpenSSLCertificate](class.opensslcertificate.md) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | У разі успішного виконання повертає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше повертався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509` |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509` |
