---
navigation:
  - function.sqlsrv-num-fields.md: « sqlsrv\_num\_fields
  - function.sqlsrv-prepare.md: sqlsrv\_prepare »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_num\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_num\_rows

(No version information available, might only be in Git)

sqlsrv\_num\_rows — Отримує кількість рядків у наборі результатів

### Опис

```methodsynopsis
sqlsrv_num_rows(resource $stmt): mixed
```

Витягує кількість рядків у наборі результатів. Функція вимагає, щоб ресурс оператора було створено за допомогою статичного курсору або курсору набору ключів. Для отримання додаткової інформації дивіться опис функцій [sqlsrv\_query()](function.sqlsrv-query.md) [sqlsrv\_prepare()](function.sqlsrv-prepare.md) або [» Вказівка ​​типу курсору та вибір рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)в документации Microsoft SQLSRV.

### Список параметрів

`stmt`

Оператор, для якого повертається кількість рядків. Ресурс оператора має бути створений за допомогою статичного курсору чи курсору набору ключів. Для отримання додаткової інформації дивіться опис функцій [sqlsrv\_query()](function.sqlsrv-query.md) [sqlsrv\_prepare()](function.sqlsrv-prepare.md) або [» Вказівка ​​типу курсору та вибір рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx)в документации Microsoft SQLSRV.

### Значення, що повертаються

Повертає кількість рядків, отриманих у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо використовується прямий курсор (за замовчуванням) або динамічний курсор, повертається **`false`**

### Приклади

**Приклад #1 Приклад використання** sqlsrv\_num\_rows()\*\*\*\*

```php
<?php
$server = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $server, $connectionInfo );

$sql = "SELECT * FROM Table_1";
$params = array();
$options =  array( "Scrollable" => SQLSRV_CURSOR_KEYSET );
$stmt = sqlsrv_query( $conn, $sql , $params, $options );

$row_count = sqlsrv_num_rows( $stmt );

if ($row_count === false)
   echo "Ошибка при получении количества строк.";
else
   echo $row_count;
?>
```

### Дивіться також

-   [sqlsrv\_has\_rows()](function.sqlsrv-has-rows.md) \- Вказує, чи має зазначений оператор рядки
-   [sqlsrv\_rows\_affected()](function.sqlsrv-rows-affected.md) \- Повертає кількість рядків, змінених останнім виконаним запитом INSERT, UPDATE чи DELETE
