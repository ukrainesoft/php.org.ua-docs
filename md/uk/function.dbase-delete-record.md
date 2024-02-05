---
navigation:
  - function.dbase-create.md: « dbase\_create
  - function.dbase-get-header-info.md: dbase\_get\_header\_info »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_delete\_record
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_delete\_record

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_delete\_record — Видалення записів з бази даних

### Опис

```methodsynopsis
dbase_delete_record(resource $database, int $number): bool
```

Позначає записи для видалення з бази даних.

> **Зауваження** :
> 
> Для остаточного видалення записів з бази даних необхідно викликати [dbase\_pack()](function.dbase-pack.md)

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

`number`

Ціле число, в проміжку від 1 до кількості записів у базі динних (кількість записів повертає функція [dbase\_numrecords()](function.dbase-numrecords.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип resource, а не int. |

### Дивіться також

-   [dbase\_add\_record()](function.dbase-add-record.md) \- Додає запис до бази даних
-   [dbase\_replace\_record()](function.dbase-replace-record.md) \- Замінює запис у базі даних
