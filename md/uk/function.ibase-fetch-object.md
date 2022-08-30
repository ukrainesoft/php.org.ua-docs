Отримує об'єкт із бази даних InterBase

-   [« ibasefetchassoc](function.ibase-fetch-assoc.html)
    
-   [ibasefetchrow »](function.ibase-fetch-row.html)
    
-   [PHP Manual](index.html)
    
-   [Функции Firebird/InterBase](ref.ibase.html)
    
-   Отримує об'єкт із бази даних InterBase
    

# ibasefetchobject

(PHP 5, PHP 7 < 7.4.0)

ibasefetchobject — Отримує об'єкт із бази даних InterBase

### Опис

```methodsynopsis
ibase_fetch_object(resource $result_id, int $fetch_flag = 0): object
```

Витягує рядок як псевдооб'єкт із заданого ідентифікатора результату.

Наступні дзвінки **ibasefetchobject()** повернуть наступний рядок у наборі результатів.

### Список параметрів

`result_id`

Ідентифікатор результату InterBase, отриманий за допомогою [ibasequery()](function.ibase-query.html) або [ibaseexecute()](function.ibase-execute.html)

`fetch_flag`

`fetch_flag` є комбінацією констант **`IBASE_TEXT`** і **`IBASE_UNIXTIME`** ORed. Передача **`IBASE_TEXT`** змусить функцію повертати вміст BLOB-об'єктів замість ідентифікаторів BLOB-об'єктів. Передача **`IBASE_UNIXTIME`** змусить функцію повертати значення дати/часу як позначки часу Unix, а не як відформатовані рядки.

### Значення, що повертаються

Повертає об'єкт з інформацією про рядок або \*\*`false`\*\*якщо рядків більше немає.

### Приклади

**Приклад #1 Приклад використання **ibasefetchobject()****

```php
<?php
$dbh = ibase_connect($host, $username, $password);
$stmt = 'SELECT * FROM tblname';
$sth = ibase_query($dbh, $stmt);
while ($row = ibase_fetch_object($sth)) {
    echo $row->email . "\n";
}
ibase_close($dbh);
?>
```

### Дивіться також

-   [ibasefetchrow()](function.ibase-fetch-row.html) - Витягує рядок із бази даних InterBase
-   [ibasefetchassoc()](function.ibase-fetch-assoc.html) - Витягує рядок результату із запиту у вигляді асоціативного масиву