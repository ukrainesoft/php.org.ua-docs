Закриває дані BLOB/CLOB

-   [« cubrid\_is\_instance](function.cubrid-is-instance.html)
    
-   [cubrid\_lob\_export »](function.cubrid-lob-export.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Закриває дані BLOB/CLOB
    

# cubridлобclose

(PECL CUBRID >= 8.3.1)

cubridлобclose — Закриває дані BLOB/CLOB

### Опис

```methodsynopsis
cubrid_lob_close(array $lob_identifier_array): bool
```

**cubridлобclose()** використовується для закриття всіх BLOB/CLOB, що повертаються функцією [cubrid\_lob\_get()](function.cubrid-lob-get.html)

### Список параметрів

`lob_identifier_array`

Масив ідентифікаторів LOB, повернутий [cubrid\_lob\_get()](function.cubrid-lob-get.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridлобclose()****

```php
<?php
$conn = cubrid_connect ("localhost", 33000, "demodb", "dba");

cubrid_execute($conn,"DROP TABLE if exists doc");
cubrid_execute($conn,"CREATE TABLE doc (id INT, doc_content CLOB)");
cubrid_execute($conn,"INSERT INTO doc VALUES (5,'hello,cubrid')");

$lobs = cubrid_lob_get($conn, "SELECT doc_content FROM doc WHERE id=5");
echo "Размер документа: ".cubrid_lob_size($lobs[0])." байтов";
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
cubrid_disconnect($conn);
?>
```

### Дивіться також

-   [cubrid\_lob\_get()](function.cubrid-lob-get.html) - Отримує дані BLOB/CLOB
-   [cubrid\_lob\_size()](function.cubrid-lob-size.html) - Отримує розмір даних BLOB/CLOB
-   [cubrid\_lob\_export()](function.cubrid-lob-export.html) - Експортує дані BLOB/CLOB у файл
-   [cubrid\_lob\_send()](function.cubrid-lob-send.html) - Читає дані BLOB/CLOB та відправляє їх прямо до браузера