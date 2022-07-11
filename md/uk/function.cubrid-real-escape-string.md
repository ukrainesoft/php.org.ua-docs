- [«cubrid_query](function.cubrid-query.md)
- [cubrid_result »](function.cubrid-result.md)

- [PHP Manual](index.md)
- [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
- Екранування спеціальних символів у SQL-запиті

#cubrid_real_escape_string

(PECL CUBRID = 8.3.0)

cubrid_real_escape_string — Екранування спеціальних символів у
SQL-запит

### Опис

**cubrid_real_escape_string**(string `$unescaped_string`, resource
`$conn_identifier` = ?): string

Функція повертає екрановану версію переданого рядка. Вона
екранує символи: **```**. В цілому, одинарна лапка використовується для
обгортання символьного рядка. Також можна використовувати подвійні лапки,
Залежно від значення ansi_quotes. Якщо ansi_quotes встановлено в
"no", то рядок обгорнутий у подвійні лапки буде розглядатися як
рядок символів, а чи не як ідентифікатор. Значення за замовчуванням – "yes".
Якщо ви хочете використовувати одинарну лапку як частину рядка -
поставте дві одинарні лапки поспіль.

### Список параметрів

`unescaped_string`
Рядок, який необхідно екранувати

`conn_identifier`
Ідентифікатор з'єднання CUBRID. Якщо не задано, то буде використано
останнє з'єднання, повернене
[cubrid_connect()](function.cubrid-connect.md).

### Значення, що повертаються

Екранований рядок.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubrid_real_escape_string()****

`` <?php$conn = cubrid_connect("localhost", 33000, "demodb");$unescaped_str = ' !"#$%&\'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLM []^_`abcdefghijklmnopqrstuvwxyz{|}~';$escaped_str =cubrid_real_escape_string($unescaped_str);$len = strlen($unescaped_str);@cubrid_execute($conn, "DROP CREATE TABLE cubrid_test (t char($len))");cubrid_execute($conn, "INSERT INTO cubrid_test (t) VALUES('$escaped_str')");$req = cubrid_execute  );$row = cubrid_fetch_assoc($req);var_dump($row);cubrid_close_request($req);cubrid_disconnect($conn);?> ``

Результат виконання цього прикладу:

array(1) {
["t"]=>
string(95) " !"#$%&'()*+,-./0123456789:;<=>?@ABCDEFGHIJKLMNOPQRSTUVWXYZ[]^_`abcdefghijklmnopqrstuvwxyz{|}~"
}
