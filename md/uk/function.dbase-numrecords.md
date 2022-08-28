Отримує кількість записів у базі даних

-   [« dbase\_numfields](function.dbase-numfields.html)
    
-   [dbase\_open »](function.dbase-open.html)
    
-   [PHP Manual](index.html)
    
-   [dBase](ref.dbase.html)
    
-   Отримує кількість записів у базі даних
    

# dbasenumrecords

(PHP 5 < 5.3.0, dbase 5, dbase 7)

dbasenumrecords — Отримує кількість записів у базі даних

### Опис

```methodsynopsis
dbase_numrecords(resource $database): int
```

Отримує кількість записів (рядків) у зазначеній базі даних.

> **Зауваження**
> 
> Записи, позначені як віддалені, також враховуються.

> **Зауваження**
> 
> Записи бази даних нумеруються від 1 `dbase_numrecords($db)`, тоді як поля від 0 до `dbase_numfields($db)-1`

### Список параметрів

`database`

Ресурс бази даних, що повертається функцією [dbase\_open()](function.dbase-open.html) або [dbase\_create()](function.dbase-create.html)

### Значення, що повертаються

Кількість записів у базі даних, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| dbase 7.0.0 | Параметр `database` тепер має тип resource, а не int. |

### Приклади

**Приклад #1 Цикл з усіх записів бази даних**

```php
<?php

// открываем в режиме для чтения
$db = dbase_open('/tmp/test.dbf', 0);

if ($db) {
  $record_numbers = dbase_numrecords($db);
  for ($i = 1; $i <= $record_numbers; $i++) {
      //выполнение каких-либо действий с записью
  }
}

?>
```

### Дивіться також

-   [dbase\_numfields()](function.dbase-numfields.html) - Отримує кількість полів бази даних