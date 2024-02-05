---
navigation:
  - function.cubrid-query.md: « cubrid\_query
  - function.cubrid-result.md: cubrid\_result »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_real\_escape\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_real\_escape\_string

(PECL CUBRID >= 8.3.0)

cubrid\_real\_escape\_string — Екранування спеціальних символів у SQL-запиті

### Опис

```methodsynopsis
cubrid_real_escape_string(string $unescaped_string, resource $conn_identifier = ?): string
```

Функція повертає екрановану версію переданого рядка. Вона екранує символи: **`'`**. Загалом одинарна лапка використовується для обгортання символьного рядка. Також можна використовувати подвійні лапки, залежно від значення ansi\_quotes. Якщо ansi\_quotes встановлено в "no", то рядок обгорнутий у подвійні лапки буде розглядатися як рядок символів, а не як ідентифікатор. Значення за промовчанням - "yes". Якщо ви хочете використовувати одинарну лапку як частину рядка - поставте дві одинарні лапки поспіль.

### Список параметрів

`unescaped_string`

Рядок, який необхідно екранувати

`conn_identifier`

Ідентифікатор з'єднання CUBRID. Якщо не встановлено, то буде використано останнє з'єднання, повернене [cubrid\_connect()](function.cubrid-connect.md)

### Значення, що повертаються

Екранований рядок.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_real\_escape\_string()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");

$unescaped_str = ' !"#$%&\'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~';
$escaped_str = cubrid_real_escape_string($unescaped_str);

$len = strlen($unescaped_str);

@cubrid_execute($conn, "DROP TABLE cubrid_test");
cubrid_execute($conn, "CREATE TABLE cubrid_test (t char($len))");
cubrid_execute($conn, "INSERT INTO cubrid_test (t) VALUES('$escaped_str')");

$req = cubrid_execute($conn, "SELECT * FROM cubrid_test");
$row = cubrid_fetch_assoc($req);

var_dump($row);

cubrid_close_request($req);
cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
array(1) {
  ["t"]=>
  string(95) " !"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[\]^_`abcdefghijklmnopqrstuvwxyz{|}~"
}
```
