---
navigation:
  - function.openssl-x509-fingerprint.md: « openssl\_x509\_fingerprint
  - function.openssl-x509-parse.md: openssl\_x509\_parse »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_x509\_free
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_x509\_free

(PHP 4 >= 4.0.6, PHP 5, PHP 7, PHP 8)

openssl\_x509\_free — Вивільняє ресурс сертифіката

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
openssl_x509_free(OpenSSLCertificate $certificate): void
```

> **Зауваження** :
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

**openssl\_x509\_free()** видаляє сертифікат із ідентифікатором `certificate`из памяти.

### Список параметрів

`certificate`

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла, оскільки не має сенсу. |
| 8.0.0 | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL X.509` |
