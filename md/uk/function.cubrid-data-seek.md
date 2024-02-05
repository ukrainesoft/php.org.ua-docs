---
navigation:
  - function.cubrid-close.md: « cubrid\_close
  - function.cubrid-db-name.md: cubrid\_db\_name »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_data\_seek
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_data\_seek

(PECL CUBRID >= 8.3.0)

cubrid\_data\_seek — Перемістити внутрішній покажчик у результуючому наборі CUBRID

### Опис

```methodsynopsis
cubrid_data_seek(resource $result, int $row_number): bool
```

Функція переміщує внутрішній покажчик у результуючому наборі CUBRID (заданим ідентифікатором запиту) на рядок із заданим номером. Може використовуватися разом із функціями типу [cubrid\_fetch\_assoc()](function.cubrid-fetch-assoc.md), які використовують значення `row_number`

### Список параметрів

`result`

Результат.

`row_number`

Бажаний номер рядка нового покажчика результату.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_data\_seek()\*\*\*\*

```php
<?php
$conn = cubrid_connect("127.0.0.1", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");
cubrid_data_seek($req, 0);

$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_data_seek($req, 2);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_data_seek($req, 4);
$result = cubrid_fetch_row($req);
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

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
