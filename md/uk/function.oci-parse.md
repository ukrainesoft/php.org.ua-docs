---
navigation:
  - function.oci-num-rows.md: « oci\_num\_rows
  - function.oci-password-change.md: oci\_password\_change »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_parse
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_parse

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_parse — Підготовка запиту до виконання

### Опис

```methodsynopsis
oci_parse(resource $connection, string $sql): resource|false
```

Готує `sql` до виконання, використовуючи з'єднання `connection` і повертає ідентифікатор виразу, який може бути використаний далі функціями[oci\_bind\_by\_name()](function.oci-bind-by-name.md),[oci\_execute()](function.oci-execute.md) та іншими.

Ідентифікатори виразів можуть бути звільнені функцією [oci\_free\_statement()](function.oci-free-statement.md)или установкой переменной в\*\*`null`\*\*

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, отриманий із функцій [oci\_connect()](function.oci-connect.md) [oci\_pconnect()](function.oci-pconnect.md) або [oci\_new\_connect()](function.oci-new-connect.md)

`sql`

Запит SQL або PL/SQL.

SQL-запити *не повинні* закінчуватися точкою з комою (";"). PL/SQL-запити *повинні* закінчуватися точкою з комою (";").

### Значення, що повертаються

Повертає дескриптор виразу у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**oci\_parse()\*\* із SQL-запитами\*\*

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

// Парсинг запроса. Обратите внимание на отсутствие точки запятой в конце SQL-запроса
$stid = oci_parse($conn, 'SELECT * FROM employees');
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

?>
```

**Пример #2 Пример использования**oci\_parse()\*\* з PL/SQL-запитами\*\*

```php
<?php

/*
  Перед запуском PHP-скрипта, создайте хранимую процедуру в
  SQL*Plus или SQL Developer:

  CREATE OR REPLACE PROCEDURE myproc(p1 IN NUMBER, p2 OUT NUMBER) AS
  BEGIN
      p2 := p1 * 2;
  END;

*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$p1 = 8;

// При парсинге PL/SQL запросов необходимо наличие точки с запятой в конце строки
$stid = oci_parse($conn, 'begin myproc(:p1, :p2); end;');
oci_bind_by_name($stid, ':p1', $p1);
oci_bind_by_name($stid, ':p2', $p2, 40);

oci_execute($stid);

print "$p2\n";   // prints 16

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження** :
> 
> Ця функція *не перевіряє*синтаксис запроса`sql`. Єдиний спосіб перевірити правильність SQL чи PL/SQL-запиту `sql` - це здійснити його.

### Дивіться також

-   [oci\_execute()](function.oci-execute.md) \- Виконує підготовлений вираз
-   [oci\_free\_statement()](function.oci-free-statement.md) \- Звільняє ресурси, які займає курсор або SQL-вираз.
