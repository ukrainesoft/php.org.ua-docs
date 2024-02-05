---
navigation:
  - function.oci-get-implicit-resultset.md: « oci\_get\_implicit\_resultset
  - function.oci-lob-is-equal.md: oci\_lob\_is\_equal »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_lob\_copy
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_lob\_copy

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_lob\_copy — Копіює об'єкт LOB

### Опис

```methodsynopsis
oci_lob_copy(OCILob $to, OCILob $from, ?int $length = null): bool
```

Копіює вміст або частину вмісту об'єкта LOB в інший об'єкт LOB. Вміст об'єкта LOB, у який виконується копіювання, перезаписується.

Якщо потрібно скопіювати певну частину об'єкта, для цього можна використовувати [OCILob::seek()](ocilob.seek.md)щоб пересунути внутрішні покажчики об'єктів на потрібні позиції.

### Список параметрів

`to`

LOB призначення.

`from`

Копіюваний об'єкт LOB.

`length`

Довжина ділянки вмісту копіювання.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0, PECL OCI8 3.0.0 | `length` тепер допускає значення null. |

### Примітки

> **Зауваження** :
> 
> Клас OCILob називався OCI-Lob до PHP 8 та PECL OCI8 3.0.0.
