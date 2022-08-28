Отримує дані BLOB/CLOB

-   [« cubrid\_lob\_export](function.cubrid-lob-export.html)
    
-   [cubrid\_lob\_send »](function.cubrid-lob-send.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримує дані BLOB/CLOB
    

# cubridлобget

(PECL CUBRID >= 8.3.1)

cubridлобget — Отримує дані BLOB/CLOB

### Опис

```methodsynopsis
cubrid_lob_get(resource $conn_identifier, string $sql): array
```

**cubridлобget()** використовується для отримання метаінформації BLOB/CLOB з бази даних CUBRID, CUBRID отримує BLOB/CLOB, виконуючи оператор SQL, і повертає все LOB як масиву ресурсів. Необхідно переконатися, що SQL повертає лише один стовпець, та його тип даних - BLOB чи CLOB.

Не варто забувати про використання [cubrid\_lob\_close()](function.cubrid-lob-close.html) для звільнення LOB, якщо вони не потрібні.

### Список параметрів

`conn_identifier`

Ідентифікатор підключення.

`sql`

Оператор SQL, що виконується.

### Значення, що повертаються

Повертає масив LOB-ресурсів у разі успішного виконання процесу або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridлобget()****

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

-   [cubrid\_lob\_close()](function.cubrid-lob-close.html) - Закриває дані BLOB/CLOB
-   [cubrid\_lob\_size()](function.cubrid-lob-size.html) - Отримує розмір даних BLOB/CLOB
-   [cubrid\_lob\_export()](function.cubrid-lob-export.html) - Експортує дані BLOB/CLOB у файл
-   [cubrid\_lob\_send()](function.cubrid-lob-send.html) - Читає дані BLOB/CLOB та відправляє їх прямо до браузера