---
navigation:
  - function.sqlsrv-has-rows.md: « sqlsrv\_has\_rows
  - function.sqlsrv-num-fields.md: sqlsrv\_num\_fields »
  - index.md: PHP Manual
  - ref.sqlsrv.md: Функції SQLSRV
title: sqlsrv\_next\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# sqlsrv\_next\_result

(No version information available, might only be in Git)

sqlsrv\_next\_result — Робить активним наступний результат вказаного оператора

### Опис

```methodsynopsis
sqlsrv_next_result(resource $stmt): mixed
```

Робить активним наступний результат вказаного оператора. Результати включають набори результатів, кількість рядків та вихідні параметри.

### Список параметрів

`stmt`

Оператор, яким викликається наступний результат.

### Значення, що повертаються

Повертає \*\*`true`**якщо наступний результат був успішно отриманий, **`false`**, если произошла ошибка и**`null`\*\*якщо результатів для отримання більше немає.

### Приклади

**Пример #1 Пример использования**sqlsrv\_next\_result()\*\*\*\*

У наступному прикладі виконується пакетний запит, який додає записи таблицю, а потім вибирає дані з таблиці. Це дає два результати оператора: один для рядків, на які впливає INSERT, і один для рядків, які повертаються SELECT. Щоб перейти до рядків, які повертаються SELECT, необхідно викликати **sqlsrv\_next\_result()**, щоб пройти повз перший результат.

```php
<?php
$serverName = "serverName\sqlexpress";
$connectionInfo = array("Database"=>"dbName", "UID"=>"userName", "PWD"=>"password");
$conn = sqlsrv_connect( $serverName, $connectionInfo);

$query = "INSERT INTO Table_1 (id, data) VALUES (?,?); SELECT * FROM TABLE_1;";
$params = array(1, "some data");
$stmt = sqlsrv_query($conn, $query, $params);

// Использовать первый результат (строки, затронутые INSERT) без вызова sqlsrv_next_result.
echo "Затронуто строк: ".sqlsrv_rows_affected($stmt)."<br />";

// Переход к следующему результату и отображение результатов.
$next_result = sqlsrv_next_result($stmt);
if( $next_result ) {
   while( $row = sqlsrv_fetch_array( $stmt, SQLSRV_FETCH_ASSOC)){
      echo $row['id'].": ".$row['data']."<br />";
   }
} elseif( is_null($next_result)) {
     echo "Больше строк нет.<br />";
} else {
     die(print_r(sqlsrv_errors(), true));
}
?>
```

### Дивіться також

-   [sqlsrv\_query()](function.sqlsrv-query.md) \- готує та виконує запит
-   [sqlsrv\_fetch\_array()](function.sqlsrv-fetch-array.md) \- Повертає рядок як масив
-   [sqlsrv\_rows\_affected()](function.sqlsrv-rows-affected.md) \- Повертає кількість рядків, змінених останнім виконаним запитом INSERT, UPDATE чи DELETE
