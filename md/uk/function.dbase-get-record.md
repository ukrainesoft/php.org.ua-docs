---
navigation:
  - function.dbase-get-record-with-names.md: « dbase\_get\_record\_with\_names
  - function.dbase-numfields.md: dbase\_numfields »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_get\_record
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_get\_record

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_get\_record — Отримує записи з бази даних, як із індексованого масиву

### Опис

```methodsynopsis
dbase_get_record(resource $database, int $number): array
```

Отримує записи з бази даних як з індексованого масиву.

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

`number`

Індекс запису (Тут відповідає фізичному номеру запису. - прим. пров.) в діапазоні від до`dbase_numrecords($dbase_identifier)`

### Значення, що повертаються

Повертає запис як масиву. Масив буде включати ключ `deleted` який дорівнює 1, якщо запис позначено видалення (дивіться [dbase\_delete\_record()](function.dbase-delete-record.md)

Кожне поле перетворюється на відповідний тип PHP, за винятком:

-   Об'єкт Date перетворюється на рядок.
-   Об'єкт DateTime перетворюється на рядок.
-   Цілі, що виходять із діапазону\*\*`PHP_INT_MIN`\*\* .. . **`PHP_INT_MAX`**, перетворюються на рядки.
-   До dbase 7.0.0 логічні значення (`L`) перетворюються на или

В случае возникновения ошибки,**dbase\_get\_record()** повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип resource, а не int. |

### Дивіться також

-   [dbase\_get\_record\_with\_names()](function.dbase-get-record-with-names.md) \- Отримує запис із бази даних у вигляді асоціативного масиву
