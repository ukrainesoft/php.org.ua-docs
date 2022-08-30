Імпортує дані BLOB/CLOB із файлу

-   [« cubridlob2export](function.cubrid-lob2-export.html)
    
-   [cubridlob2new »](function.cubrid-lob2-new.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Імпортує дані BLOB/CLOB із файлу
    

# cubridlob2import

(PECL CUBRID >= 8.4.1)

cubridlob2import — Імпортує дані BLOB/CLOB із файлу

### Опис

```methodsynopsis
cubrid_lob2_import(resource $lob_identifier, string $file_name): bool
```

Функція **cubridlob2import()** використовується для збереження вмісту BLOB/CLOB з файлу. Щоб використовувати цю функцію, потрібно використовувати [cubridlob2new()](function.cubrid-lob2-new.html) або спочатку отримати LOB-об'єкт із бази даних CUBRID. Якщо файл існує, операція завершиться помилкою. Функція не впливатиме на положення курсору LOB-об'єкта. Вона керує всім LOB-об'єктом.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, отриманий у результаті [cubridlob2new()](function.cubrid-lob2-new.html) або отриманий із набору результатів.

`filename`

Ім'я файлу, до якого ви хочете імпортувати дані BLOB/CLOB. Також підтримується шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання [cubridlob2export()](function.cubrid-lob2-export.html)**

```php
<?php

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists test_lob");
cubrid_execute($conn,"CREATE TABLE test_lob (id INT, contents CLOB)");

$req = cubrid_prepare($conn, "INSERT INTO test_lob VALUES (?, ?)");
cubrid_bind($req, 1, 1);

$lob = cubrid_lob2_new($conn, "clob");
cubrid_lob2_import($lob, "doc_1.txt");
cubrid_lob2_bind($req, 2, $lob, 'CLOB'); // или cubrid_lob2_bind($req, 2, $lob);

cubrid_execute($req);

cubrid_lob2_close($lob);
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubridlob2new()](function.cubrid-lob2-new.html) - Створює об'єкт LOB
-   [cubridlob2close()](function.cubrid-lob2-close.html) - Закриває об'єкт LOB
-   [cubridlob2export()](function.cubrid-lob2-export.html) - Експортує LOB-об'єкт у файл
-   [cubridlob2bind()](function.cubrid-lob2-bind.html) - Зв'язує об'єкт LOB або рядок у вигляді об'єкта LOB з підготовленим оператором як параметри