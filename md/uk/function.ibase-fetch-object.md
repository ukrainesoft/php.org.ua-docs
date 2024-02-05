---
navigation:
  - function.ibase-fetch-assoc.md: « ibase\_fetch\_assoc
  - function.ibase-fetch-row.md: ibase\_fetch\_row »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_fetch\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_fetch\_object

(PHP 5, PHP 7 < 7.4.0)

ibase\_fetch\_object — Отримує об'єкт із бази даних InterBase

### Опис

```methodsynopsis
ibase_fetch_object(resource $result_id, int $fetch_flag = 0): object
```

Витягує рядок як псевдооб'єкт із заданого ідентифікатора результату.

Наступні дзвінки \*\*ibase\_fetch\_object()\*\*вернут следующую строку в наборе результатов.

### Список параметрів

`result_id`

Ідентифікатор результату InterBase, отриманий за допомогою [ibase\_query()](function.ibase-query.md) або [ibase\_execute()](function.ibase-execute.md)

`fetch_flag`

`fetch_flag` є комбінацією констант **`IBASE_TEXT`** і **`IBASE_UNIXTIME`**ORed. Передача**`IBASE_TEXT`** змусить функцію повертати вміст BLOB-об'єктів замість ідентифікаторів BLOB-об'єктів. Передача **`IBASE_UNIXTIME`** змусить функцію повертати значення дати/часу як позначки часу Unix, а не як відформатовані рядки.

### Значення, що повертаються

Повертає об'єкт з інформацією про рядок або \*\*`false`\*\*якщо рядків більше немає.

### Приклади

**Приклад #1 Приклад використання** ibase\_fetch\_object()\*\*\*\*

```php
<?php
$dbh = ibase_connect($host, $username, $password);
$stmt = 'SELECT * FROM tblname';
$sth = ibase_query($dbh, $stmt);
while ($row = ibase_fetch_object($sth)) {
    echo $row->email . "\n";
}
ibase_close($dbh);
?>
```

### Дивіться також

-   [ibase\_fetch\_row()](function.ibase-fetch-row.md) \- Витягує рядок із бази даних InterBase
-   [ibase\_fetch\_assoc()](function.ibase-fetch-assoc.md) \- Витягує рядок результату із запиту у вигляді асоціативного масиву
