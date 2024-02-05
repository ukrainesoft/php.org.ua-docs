---
navigation:
  - function.openssl-pkey-export.md: « openssl\_pkey\_export
  - function.openssl-pkey-get-details.md: openssl\_pkey\_get\_details »
  - index.md: PHP Manual
  - ref.openssl.md: Функції OpenSSL
title: openssl\_pkey\_free
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# openssl\_pkey\_free

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

openssl\_pkey\_free — Звільняє ресурс закритого ключа

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
openssl_pkey_free(OpenSSLAsymmetricKey $key): void
```

> **Зауваження** :
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Функція вивільняє ресурс закритого ключа, створений [openssl\_pkey\_new()](function.openssl-pkey-new.md)

### Список параметрів

`key`

Ресурс, що містить ключ.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Функція застаріла, оскільки не має сенсу. |
| 8.0.0 | `key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу`OpenSSL key` |
