---
navigation:
  - function.cubrid-lob-send.md: « cubrid\_lob\_send
  - function.cubrid-lob2-bind.md: cubrid\_lob2\_bind »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_lob\_size
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_lob\_size

(PECL CUBRID >= 8.3.1)

cubrid\_lob\_size — Отримує розмір даних BLOB/CLOB

### Опис

```methodsynopsis
cubrid_lob_size(resource $lob_identifier): string
```

**cubrid\_lob\_size()** використовується для отримання даних BLOB/CLOB.

### Список параметрів

`lob_identifier`

Ідентифікатор LOB.

### Значення, що повертаються

Рядок, що представляє розмір LOB-даних у разі успішного виконання процесу, або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.4.0 | Тип значення, що повертається змінений з int на string. |

### Приклади

**Приклад #1 Приклад використання** cubrid\_lob\_size()\*\*\*\*

```php
<?php
$lobs = cubrid_lob_get($con, "SELECT doc_content FROM doc WHERE doc_id=5");
echo "Размер документа:".cubrid_lob_size($lobs[0]);
cubrid_lob_export($conn, $lobs[0], "doc_5.txt");
cubrid_lob_close($lobs);
?>
```

### Дивіться також

-   [cubrid\_lob\_get()](function.cubrid-lob-get.md) \- Отримує дані BLOB/CLOB
-   [cubrid\_lob\_close()](function.cubrid-lob-close.md) \- Закриває дані BLOB/CLOB
-   [cubrid\_lob\_export()](function.cubrid-lob-export.md) \- Експортує дані BLOB/CLOB у файл
-   [cubrid\_lob\_send()](function.cubrid-lob-send.md) \- Читає дані BLOB/CLOB та відправляє їх прямо до браузера
