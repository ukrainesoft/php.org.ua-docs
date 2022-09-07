---
navigation:
  - function.dbase-create.md: « dbasecreate
  - function.dbase-get-header-info.md: dbasegetheaderinfo »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbasedeleterecord
---
# dbasedeleterecord

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasedeleterecord — Видалення записів з бази даних

### Опис

```methodsynopsis
dbase_delete_record(resource $database, int $number): bool
```

Позначає записи для видалення з бази даних.

> **Зауваження**
> 
> Для остаточного видалення записів з бази даних необхідно викликати [dbasepack()](function.dbase-pack.md)

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbaseopen()](function.dbase-open.md) або [dbasecreate()](function.dbase-create.md)

`number`

Ціле число, в проміжку від 1 до кількості записів у базі динних (кількість записів повертає функція [dbasenumrecords()](function.dbase-numrecords.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Дивіться також

-   [dbaseaddrecord()](function.dbase-add-record.md) - Додає запис до бази даних
-   [dbasereplacerecord()](function.dbase-replace-record.md) - Замінює запис у базі даних
