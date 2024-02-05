---
navigation:
  - function.oci-lob-is-equal.md: « oci\_lob\_is\_equal
  - function.oci-new-connect.md: oci\_new\_connect »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_new\_collection
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_new\_collection

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_new\_collection — Створює новий об'єкт колекції

### Опис

```methodsynopsis
oci_new_collection(resource $connection, string $type_name, ?string $schema = null): OCICollection|false
```

Створює новий об'єкт колекції.

### Список параметрів

`connection`

Ідентифікатор з'єднання з сервером Oracle, який повертається функцією [oci\_connect()](function.oci-connect.md) або [oci\_pconnect()](function.oci-pconnect.md)

`type_name`

Має бути коректним ім'ям типу (у верхньому регістрі).

`schema`

Має бути зазначена схема даних, де створено іменований тип. Якщо передано значення **`null`**, вказується ім'я користувача як ім'я схеми.

### Значення, що повертаються

Повертає новий об'єкт [OCICollection](class.ocicollection.md)или\*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `schema` тепер допускає значення null. |

### Примітки

> **Зауваження** :
> 
> Класс[OCICollection](class.ocicollection.md) називався **OCI-Collection** до PHP 8 та OCI8 3.0.0.
