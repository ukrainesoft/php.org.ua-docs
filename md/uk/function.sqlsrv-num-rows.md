---
navigation:
  - function.sqlsrv-num-fields.html: « sqlsrvnumfields
  - function.sqlsrv-prepare.html: sqlsrvprepare »
  - index.html: PHP Manual
  - ref.sqlsrv.html: Функції SQLSRV
title: sqlsrvnumrows
---
# sqlsrvnumrows

(No version information available, might only be in Git)

sqlsrvnumrows — Отримує кількість рядків у наборі результатів

### Опис

```methodsynopsis
sqlsrv_num_rows(resource $stmt): mixed
```

Витягує кількість рядків у наборі результатів. Функція вимагає, щоб ресурс оператора було створено за допомогою статичного курсору або курсору набору ключів. Для отримання додаткової інформації дивіться опис функцій [sqlsrvquery()](function.sqlsrv-query.html) [sqlsrvprepare()](function.sqlsrv-prepare.html) або [» Вказівка ​​типу курсору та вибір рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx) у документації Microsoft SQLSRV.

### Список параметрів

`stmt`

Оператор, для якого повертається кількість рядків. Ресурс оператора має бути створений за допомогою статичного курсору чи курсору набору ключів. Для отримання додаткової інформації дивіться опис функцій [sqlsrvquery()](function.sqlsrv-query.html) [sqlsrvprepare()](function.sqlsrv-prepare.html) або [» Вказівка ​​типу курсору та вибір рядків](http://msdn.microsoft.com/en-us/library/ee376927.aspx) у документації Microsoft SQLSRV.

### Значення, що повертаються

Повертає кількість рядків, отриманих у разі успішного виконання або **`false`** у разі виникнення помилки. Якщо використовується прямий курсор (за замовчуванням) або динамічний курсор, повертається **`false`**

### Приклади

**Приклад #1 Приклад використання **sqlsrvnumrows()****

```php
<?php
$server = "serverName\sqlexpress";
$connectionInfo = array( "Database"=>"dbName", "UID"=>"username", "PWD"=>"password" );
$conn = sqlsrv_connect( $server, $connectionInfo );

$sql = "SELECT * FROM Table_1";
$params = array();
$options =  array( "Scrollable" => SQLSRV_CURSOR_KEYSET );
$stmt = sqlsrv_query( $conn, $sql , $params, $options );

$row_count = sqlsrv_num_rows( $stmt );

if ($row_count === false)
   echo "Ошибка при получении количества строк.";
else
   echo $row_count;
?>
```

### Дивіться також

-   [sqlsrvhasrows()](function.sqlsrv-has-rows.html) - Вказує, чи має вказаний оператор рядки
-   [sqlsrvrowsaffected()](function.sqlsrv-rows-affected.html) - Повертає кількість рядків, змінених останнім виконаним запитом INSERT, UPDATE чи DELETE
