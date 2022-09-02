---
navigation:
  - function.oci-lob-is-equal.md: « ocilobісequal
  - function.oci-new-connect.md: ocinewconnect »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocinewcollection
---
# ocinewcollection

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocinewcollection — Створює новий об'єкт колекції

### Опис

```methodsynopsis
oci_new_collection(resource $connection, string $type_name, ?string $schema = null): OCICollection|false
```

Створює новий об'єкт колекції.

### Список параметрів

`connection`

Ідентифікатор з'єднання з сервером Oracle, який повертається функцією [ociconnect()](function.oci-connect.md) або [ocipconnect()](function.oci-pconnect.md)

`type_name`

Має бути коректним ім'ям типу (у верхньому регістрі).

`schema`

Має бути зазначена схема даних, де створено іменований тип. Якщо передано значення **`null`**, вказується ім'я користувача як ім'я схеми.

### Значення, що повертаються

Повертає новий об'єкт [OCICollection](class.ocicollection.md) або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `schema` тепер допускає значення null. |

### Примітки

> **Зауваження**
> 
> Клас [OCICollection](class.ocicollection.md) називався **OCI-Collection** до PHP 8 та OCI8 3.0.0.

> **Зауваження**
> 
> У версіях PHP нижче 5.0.0 ця функція називалася [ocinewcollection()](function.ocinewcollection.md). У PHP 5.0.0 і вище [ocinewcollection()](function.ocinewcollection.md) є аліасом \*\*ocinewcollection()\*\*Тому ви можете продовжувати використовувати це ім'я, однак це не рекомендується.
