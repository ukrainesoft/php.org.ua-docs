---
navigation:
  - function.dbase-get-header-info.md: « dbase\_get\_header\_info
  - function.dbase-get-record.md: dbase\_get\_record »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_get\_record\_with\_names
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_get\_record\_with\_names

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_get\_record\_with\_names — Отримує запис із бази даних у вигляді асоціативного масиву

### Опис

```methodsynopsis
dbase_get_record_with_names(resource $database, int $number): array
```

Отримує запис із бази даних dBase у вигляді асоціативного масиву (разом із іменами відповідних полів).

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

`number`

Індекс запису (тут відповідає фізичному номеру запису. — прим. перекл.) в діапазоні від до`dbase_numrecords($dbase_identifier)`

### Значення, що повертаються

Асоціативний масив із даними рядка. Масив міститиме ключ `deleted`, який дорівнює 1, якщо запис позначено видалення (дивіться опис функції [dbase\_delete\_record()](function.dbase-delete-record.md)). Повертає і пусті записи. Тому цією функцією неможливо отримати значення або ім'я поля `delete`

Кожне поле перетворюється на відповідний тип PHP, за винятком:

-   Об'єкт Date перетворюється на рядок.
-   Об'єкт DateTime перетворюється на рядок.
-   Цілі, що виходять із діапазону\*\*`PHP_INT_MIN`\*\* .. . **`PHP_INT_MAX`**, перетворюються на рядки.
-   До dbase 7.0.0 логічні значення (`L`) перетворюються на или

В случае возникновения ошибки функция**dbase\_get\_record\_with\_names()** повертає **`false`**

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип ресурсу, а не int. |

### Приклади

**Приклад #1 Список усіх зареєстрованих користувачів у базі даних**

```php
<?php
// открываем базу в режиме чтения
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      $row = dbase_get_record_with_names($db, $i);
      if ($row['ismember'] == 1) {
          echo "Member #$i: " . trim($row['name']) . "\n";
      }
  }
}
// Прим. пер. -
// к полученным с помощью dbase_get_record_with_names значениям записи
// обращаемся по имени - $row['ismember'],
// а в случае с dbase_get_record к значениям записи
// обращаемся по номеру - $row[4]
?>
```

### Дивіться також

-   [dbase\_get\_record()](function.dbase-get-record.md) \- Отримує записи з бази даних, як із індексованого масиву
