Отримує кількість рядків у наборі результатів

-   [« sqlsrv\_num\_fields](function.sqlsrv-num-fields.html)
    
-   [sqlsrv\_prepare »](function.sqlsrv-prepare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции SQLSRV](ref.sqlsrv.html)
    
-   Отримує кількість рядків у наборі результатів
    

# sqlsrvnumrows

(No version information available, might only be in Git)

sqlsrvnumrows — Отримує кількість рядків у наборі результатів

### Опис

```methodsynopsis
sqlsrv_num_rows(resource $stmt): mixed
```

Витягує кількість рядків у наборі результатів. Функція вимагає, щоб ресурс оператора було створено за допомогою статичного курсору або курсору набору ключів. Для отримання додаткової інформації дивіться опис функцій [sqlsrv\_query()](function.sqlsrv-query.html) [sqlsrv\_prepare()](function.sqlsrv-prepare.html) або [» Указание типа курсора и выбор строк](http://msdn.microsoft.com/en-us/library/ee376927.aspx) у документації Microsoft SQLSRV.

### Список параметрів

`stmt`

Оператор, для якого повертається кількість рядків. Ресурс оператора має бути створений за допомогою статичного курсору чи курсору набору ключів. Для отримання додаткової інформації дивіться опис функцій [sqlsrv\_query()](function.sqlsrv-query.html) [sqlsrv\_prepare()](function.sqlsrv-prepare.html) або [» Указание типа курсора и выбор строк](http://msdn.microsoft.com/en-us/library/ee376927.aspx) у документації Microsoft SQLSRV.

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

-   [sqlsrv\_has\_rows()](function.sqlsrv-has-rows.html) - Вказує, чи має вказаний оператор рядки
-   [sqlsrv\_rows\_affected()](function.sqlsrv-rows-affected.html) - Повертає кількість рядків, змінених останнім виконаним запитом INSERT, UPDATE чи DELETE