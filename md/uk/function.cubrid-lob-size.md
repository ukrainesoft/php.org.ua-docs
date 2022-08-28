Отримує розмір даних BLOB/CLOB

-   [« cubrid\_lob\_send](function.cubrid-lob-send.html)
    
-   [cubrid\_lob2\_bind »](function.cubrid-lob2-bind.html)
    
-   [PHP Manual](index.html)
    
-   [Функции CUBRID](ref.cubrid.html)
    
-   Отримує розмір даних BLOB/CLOB
    

# cubridлобsize

(PECL CUBRID >= 8.3.1)

cubridлобsize — Отримує розмір даних BLOB/CLOB

### Опис

```methodsynopsis
cubrid_lob_size(resource $lob_identifier): string
```

**cubridлобsize()** використовується для отримання даних BLOB/CLOB.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB.

### Значення, що повертаються

Рядок, що представляє розмір LOB-даних у разі успішного виконання процесу, або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание                                                |
|--------|---------------------------------------------------------|
|        | Тип значення, що повертається змінений з int на string. |

### Приклади

**Приклад #1 Приклад використання **cubridлобsize()****

```php
<?php
$lobs = cubrid_lob_get($con, "SELECT doc_content FROM doc WHERE doc_id=5");
echo "Размер документа:".cubrid_lob_size($lobs[0]);
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
?>
```

### Дивіться також

-   [cubrid\_lob\_get()](function.cubrid-lob-get.html) - Отримує дані BLOB/CLOB
-   [cubrid\_lob\_close()](function.cubrid-lob-close.html) - Закриває дані BLOB/CLOB
-   [cubrid\_lob\_export()](function.cubrid-lob-export.html) - Експортує дані BLOB/CLOB у файл
-   [cubrid\_lob\_send()](function.cubrid-lob-send.html) - Читає дані BLOB/CLOB та відправляє їх прямо до браузера