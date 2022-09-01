---
navigation:
  - function.openssl-x509-fingerprint.html: « opensslx509fingerprint
  - function.openssl-x509-parse.html: opensslx509parse »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslx509free
---
# opensslx509free

(PHP 4> = 4.0.6, PHP 5, PHP 7, PHP 8)

opensslx509free — Вивільняє ресурс сертифіката

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
openssl_x509_free(OpenSSLCertificate $certificate): void
```

> **Зауваження**
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

**opensslx509free()** видаляє сертифікат із ідентифікатором `certificate` із пам'яті.

### Список параметрів

`certificate`

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла, оскільки не має сенсу. |
|  | `certificate` тепер приймає екземпляр [OpenSSLCertificate](class.opensslcertificate.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL X.509` |
