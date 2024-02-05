---
navigation:
  - function.openssl-error-string.md: « openssl\_error\_string
  - function.openssl-get-cert-locations.md: openssl\_get\_cert\_locations »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_free\_key
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_free\_key

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

openssl\_free\_key — Вивільнення ресурсу ключа

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
openssl_free_key(OpenSSLAsymmetricKey $key): void
```

**openssl\_free\_key()** видаляє ключ, пов'язаний із заданим ідентифікатором `key`из памяти.

### Список параметрів

`key`

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла, оскільки не має сенсу. |
| 8.0.0 | `key`тепер приймає[OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше приймала ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |
