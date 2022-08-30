Експортує LOB-об'єкт у файл

-   [« cubridlob2close](function.cubrid-lob2-close.html)
    
-   [cubridlob2import »](function.cubrid-lob2-import.html)
    
-   [PHP Manual](index.md)
    
-   [Функции CUBRID](ref.cubrid.md)
    
-   Експортує LOB-об'єкт у файл
    

# cubridlob2export

(PECL CUBRID >= 8.4.1)

cubridlob2export — Експортує LOB-об'єкт у файл

### Опис

```methodsynopsis
cubrid_lob2_export(resource $lob_identifier, string $file_name): bool
```

Функція **cubridlob2export()** використовується для збереження вмісту даних BLOB/CLOB у файл. Щоб використовувати цю функцію, потрібно використовувати [cubridlob2new()](function.cubrid-lob2-new.html) або спочатку отримати LOB-об'єкт із бази даних CUBRID. Якщо файл існує, операція завершиться помилкою. Функція не впливатиме на положення курсору LOB-об'єкта. Вона керує всім LOB-об'єктом.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB, отриманий у результаті [cubridlob2new()](function.cubrid-lob2-new.html) або отриманий із набору результатів.

`filename`

Ім'я файлу, до якого ви хочете імпортувати дані BLOB/CLOB. Також підтримується шлях до файлу.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridlob2export()****

```php
<?php
// Таблица: test_lob (id INT, contents CLOB)

$conn = cubrid_connect("localhost", 33000, "demodb", "dba", "");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$req = cubrid_prepare($conn, "select * from doc");

cubrid_execute($req);

cubrid_move_cursor($req, 1, CUBRID_CURSOR_FIRST);

$row = cubrid_fetch($req, CUBRID_NUM | CUBRID_LOB);

cubrid_lob2_export($row[1], "doc_3.txt");

cubrid_lob2_close($row[1]);
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubridlob2new()](function.cubrid-lob2-new.html) - Створює об'єкт LOB
-   [cubridlob2close()](function.cubrid-lob2-close.html) - Закриває об'єкт LOB
-   [cubridlob2import()](function.cubrid-lob2-import.html) - Імпортує дані BLOB/CLOB із файлу
-   [cubridlob2bind()](function.cubrid-lob2-bind.html) - Зв'язує об'єкт LOB або рядок у вигляді об'єкта LOB з підготовленим оператором як параметри