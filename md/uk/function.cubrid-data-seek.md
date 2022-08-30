Перемістити внутрішній покажчик у результуючому наборі CUBRID

-   [« cubridclose](function.cubrid-close.html)
    
-   [cubridдбname »](function.cubrid-db-name.html)
    
-   [PHP Manual](index.md)
    
-   [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
    
-   Перемістити внутрішній покажчик у результуючому наборі CUBRID
    

# cubriddataseek

(PECL CUBRID >= 8.3.0)

cubriddataseek — Перемістити внутрішній покажчик у результуючому наборі CUBRID

### Опис

```methodsynopsis
cubrid_data_seek(resource $result, int $row_number): bool
```

Функція переміщує внутрішній покажчик у результуючому наборі CUBRID (заданим ідентифікатором запиту) на рядок із заданим номером. Може використовуватися разом із функціями типу [cubridfetchassoc()](function.cubrid-fetch-assoc.html), які використовують значення `row_number`

### Список параметрів

`result`

Результат.

`row_number`

Бажаний номер рядка нового покажчика результату.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubriddataseek()****

```php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");
cubrid_data_seek($req, 0);

$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_data_seek($req, 2);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_data_seek($req, 4);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
array(2) {
  [0]=>
  string(1) "X"
  [1]=>
  string(5) "Mixed"
}
array(2) {
  [0]=>
  string(1) "M"
  [1]=>
  string(3) "Man"
}
array(2) {
  [0]=>
  string(1) "S"
  [1]=>
  string(6) "Silver"
}
```