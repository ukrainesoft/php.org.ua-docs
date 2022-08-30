Робить активним наступний результат вказаного оператора

-   [« sqlsrvhasrows](function.sqlsrv-has-rows.html)
    
-   [sqlsrvnumfields »](function.sqlsrv-num-fields.html)
    
-   [PHP Manual](index.html)
    
-   [Функції SQLSRV](ref.sqlsrv.html)
    
-   Робить активним наступний результат вказаного оператора
    

# sqlsrvnextresult

(No version information available, might only be in Git)

sqlsrvnextresult — Робить активним наступний результат вказаного оператора

### Опис

```methodsynopsis
sqlsrv_next_result(resource $stmt): mixed
```

Робить активним наступний результат вказаного оператора. Результати включають набори результатів, кількість рядків та вихідні параметри.

### Список параметрів

`stmt`

Оператор, яким викликається наступний результат.

### Значення, що повертаються

Повертає \*\*`true`\*\*якщо наступний результат був успішно отриманий, **`false`**, якщо сталася помилка та \*\*`null`\*\*якщо результатів для отримання більше немає.

### Приклади

**Приклад #1 Приклад використання **sqlsrvnextresult()****

У наступному прикладі виконується пакетний запит, який додає записи таблицю, а потім вибирає дані з таблиці. Це дає два результати оператора: один для рядків, на які впливає INSERT, і один для рядків, які повертаються SELECT. Щоб перейти до рядків, які повертаються SELECT, необхідно викликати **sqlsrvnextresult()**, щоб пройти повз перший результат.

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array("Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

$query = "INSERT INTO Table_1 (id, data) VALUES (?,?); SELECT * FROM TABLE_1;";
$params = array(1, "some data");
$stmt = sqlsrv_query($conn, $query, $params);

// Использовать первый результат (строки, затронутые INSERT) без вызова sqlsrv_next_result.
echo "Затронуто строк: ".sqlsrv_rows_affected($stmt)."<br />";

// Переход к следующему результату и отображение результатов.
$next_result = sqlsrv_next_result($stmt);
if( $next_result ) {
   while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_ASSOC)){
      echo $row['id'].": ".$row['data']."<br />";
   }
} elseif( is_null($next_result)) {
     echo "Больше строк нет.<br />";
} else {
     die(print_r(sqlsrv_errors(), true));
}
?>
```

### Дивіться також

-   [sqlsrvquery()](function.sqlsrv-query.html) - готує та виконує запит
-   [sqlsrvfetcharray()](function.sqlsrv-fetch-array.html) - Повертає рядок як масив
-   [sqlsrvrowsaffected()](function.sqlsrv-rows-affected.html) - Повертає кількість рядків, змінених останнім виконаним запитом INSERT, UPDATE чи DELETE