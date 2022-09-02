---
navigation:
  - function.openssl-pkey-export.md: « opensslpkeyexport
  - function.openssl-pkey-get-details.md: opensslpkeygetdetails »
  - index.md: PHP Manual
  - ref.openssl.md: Функции OpenSSL
title: opensslpkeyfree
---
# opensslpkeyfree

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

opensslpkeyfree — Звільняє ресурс закритого ключа

**Увага**

Ця функція була *ВИДАЛЕНО* у PHP 8.0.0. Використання цієї функції не рекомендується.

### Опис

```methodsynopsis
openssl_pkey_free(OpenSSLAsymmetricKey $key): void
```

> **Зауваження**
> 
> Використання функції не має сенсу. До PHP 8.0.0 вона використовувалася для закриття ресурсу.

Функція вивільняє ресурс закритого ключа, створений [opensslpkeynew()](function.openssl-pkey-new.md)

### Список параметрів

`key`

Ресурс, що містить ключ.

### Значення, що повертаються

Функція не повертає значення після виконання.

### список змін

| Версия | Описание |
| --- | --- |
|  | Функція застаріла, оскільки не має сенсу. |
|  | `key` тепер приймає екземпляр [OpenSSLAsymmetricKey](class.opensslasymmetrickey.md); раніше приймався ресурс ([resource](language.types.resource.md)) типу `OpenSSL key` |
