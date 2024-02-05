---
navigation:
  - function.dbase-get-record.md: « dbase\_get\_record
  - function.dbase-numrecords.md: dbase\_numrecords »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbase\_numfields
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# dbase\_numfields

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbase\_numfields — Отримує кількість полів бази даних

### Опис

```methodsynopsis
dbase_numfields(resource $database): int
```

Отримує кількість полів (колонок) у вказаній базі даних.

> **Зауваження** :
> 
> Поле номеруются от 0 до`dbase_numfields($db)-1`, тоді як записи бази даних від 1 до `dbase_numrecords($db)`

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.md) або [dbase\_create()](function.dbase-create.md)

### Значення, що повертаються

Кількість полів у базі даних або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| dbase 7.0.0 | Параметр`database` тепер має тип ресурсу, а не int. |

### Приклади

**Приклад #1 Приклад використання** dbase\_numfields()\*\*\*\*

```php
<?php
//открытие БД для чтения
$db = dbase_open('.\tmp\test.dbf', 0);

//если соединение успешно, то выполняем действия
if ($db) {
  //получение количества записей БД
  $record_numbers = dbase_numrecords($db);
  //получение количества полей БД
  $nf  = dbase_numfields($db);
  //вывод всех записей БД
  //построчный обход
  for ($j = 1;  $j <= $record_numbers;  $j++) {
    //вывод номера строки
    echo $j."=>" ;
    //получение строки по номеру (индексу)
    $rec = dbase_get_record($db, $j);

    //обход по столбцам
    for ($i = 0; $i < $nf; $i++) {
      //вывод данных поля
      echo $rec[$i], "\t";
    }
  echo "<br>";
  }
dbase_close($db);
} else echo "Не удалось подключиться к БД";

?>
```

### Дивіться також

-   [dbase\_numrecords()](function.dbase-numrecords.md) \- Отримує кількість записів у базі даних
