Отримує запис із бази даних у вигляді асоціативного масиву

-   [« dbasegetheaderinfo](function.dbase-get-header-info.html)
    
-   [dbasegetrecord »](function.dbase-get-record.html)
    
-   [PHP Manual](index.html)
    
-   [dBase](ref.dbase.html)
    
-   Отримує запис із бази даних у вигляді асоціативного масиву
    

# dbasegetrecordwithnames

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasegetrecordwithnames — Отримує запис із бази даних у вигляді асоціативного масиву

### Опис

```methodsynopsis
dbase_get_record_with_names(resource $database, int $number): array
```

Отримує запис із бази даних dBase у вигляді асоціативного масиву (разом із іменами відповідних полів).

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbaseopen()](function.dbase-open.html) або [dbasecreate()](function.dbase-create.html)

`number`

Індекс запису (Тут відповідає фізичному номеру запису. - прим. пров.) в діапазоні від `1` до `dbase_numrecords($dbase_identifier)`

### Значення, що повертаються

Асоціативний масив із даними рядка. Масив буде включати ключ `deleted` який дорівнює 1, якщо запис позначено видалення (дивіться [dbasedeleterecord()](function.dbase-delete-record.html)). Повертає і пусті записи. Отже, цією функцією неможливо отримати значення чи ім'я поля `delete`

Кожне поле перетворюється на відповідний тип PHP, за винятком:

-   Date перетворюється на рядок.
-   DateTime перетворюється на рядок.
-   Цілі, що виходять із діапазону **`PHP_INT_MIN`\*\*\*\*`PHP_INT_MAX`** перетворюються на рядки.
-   До dbase 7.0.0, логічні значення (`L`) перетворюються на `1` або `0`

У разі виникнення помилки, **dbasegetrecordwithnames()** повертає **`false`**

### список змін

| Версия      | Описание                                              |
|-------------|-------------------------------------------------------|
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Список усіх зареєстрованих користувачів у базі даних**

```php
<?php
// открываем базу в режиме чтения
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      $row = dbase_get_record_with_names($db, $i);
      if ($row['ismember'] == 1) {
          echo "Member #$i: " . trim($row['name']) . "\n";
      }
  }
}
// Прим. пер. -
// к полученным с помощью dbase_get_record_with_names значениям записи
// обращаемся по имени - $row['ismember'],
// а в случае с dbase_get_record к значениям записи
// обращаемся по номеру - $row[4]
?>
```

### Дивіться також

-   [dbasegetrecord()](function.dbase-get-record.html) - Отримує записи з бази даних, як із індексованого масиву