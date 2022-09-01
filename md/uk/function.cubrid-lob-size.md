---
navigation:
  - function.cubrid-lob-send.html: « cubridlobsend
  - function.cubrid-lob2-bind.html: cubridlob2bind »
  - index.html: PHP Manual
  - ref.cubrid.html: Функции CUBRID
title: cubridлобsize
---
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

| Версия | Описание |
| --- | --- |
|  | Тип значення, що повертається змінений з int на string. |

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

-   [cubridlobget()](function.cubrid-lob-get.html) - Отримує дані BLOB/CLOB
-   [cubridlobclose()](function.cubrid-lob-close.html) - Закриває дані BLOB/CLOB
-   [cubridlobexport()](function.cubrid-lob-export.html) - Експортує дані BLOB/CLOB у файл
-   [cubridlobsend()](function.cubrid-lob-send.html) - Читає дані BLOB/CLOB та відправляє їх прямо до браузера
