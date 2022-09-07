---
navigation:
  - function.dbase-get-record.md: « dbasegetrecord
  - function.dbase-numrecords.md: dbasenumrecords »
  - index.md: PHP Manual
  - ref.dbase.md: dBase
title: dbasenumfields
---
# dbasenumfields

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasenumfields — Отримує кількість полів бази даних

### Опис

```methodsynopsis
dbase_numfields(resource $database): int
```

Отримує кількість полів (колонок) у вказаній базі даних.

> **Зауваження**
> 
> Поле нумеруються від 0 до `dbase_numfields($db)-1`, тоді як записи бази даних від 1 до `dbase_numrecords($db)`

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbaseopen()](function.dbase-open.md) або [dbasecreate()](function.dbase-create.md)

### Значення, що повертаються

Кількість полів у базі даних або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип ресурсу, а не int. |

### Приклади

**Приклад #1 Приклад використання **dbasenumfields()****

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

-   [dbasenumrecords()](function.dbase-numrecords.md) - Отримує кількість записів у базі даних
