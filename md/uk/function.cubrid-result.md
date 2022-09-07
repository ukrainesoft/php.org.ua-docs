---
navigation:
  - function.cubrid-real-escape-string.md: « cubridrealescapestring
  - function.cubrid-unbuffered-query.md: cubridunbufferedquery »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubridresult
---
# cubridresult

(PECL CUBRID >= 8.3.0)

cubridresult — Отримати значення із заданого стовпця заданого рядка

### Опис

```methodsynopsis
cubrid_result(resource $result, int $row, mixed $field = 0): string
```

Функція повертає значення із заданого стовпця заданого рядка результуючого набору.

### Список параметрів

`result`

`result` отриманий з [cubridexecute()](function.cubrid-execute.md)

`row`

Номер рядка починаючи з 0.

`field`

Ім'я або індекс стовпця `field`. Це може бути індекс, ім'я шпальти, ім'я таблиці з ім'ям шпальти, розділених точкою (tablename.fieldname). Якщо ім'я стовпця є псевдонімом ('select foo as bar from...'), використовуйте цей псевдонім замість реального імені стовпця. Якщо не задано, то буде використано перший стовпець.

### Значення, що повертаються

Значення заданого стовпця у разі успішного виконання (NULL, якщо значення null).

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridresult()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$req = cubrid_execute($conn, "SELECT * FROM code");

$result = cubrid_result($req, 0);
var_dump($result);

$result = cubrid_result($req, 0, 1);
var_dump($result);

$result = cubrid_result($req, 5, "f_name");
var_dump($result);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
string(1) "X"
string(5) "Mixed"
string(4) "Gold"
```
