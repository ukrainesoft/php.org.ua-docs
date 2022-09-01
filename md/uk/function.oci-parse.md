---
navigation:
  - function.oci-num-rows.html: « ocinumrows
  - function.oci-password-change.html: ocipasswordchange »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ociparse
---
# ociparse

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ociparse — Підготовка запиту до виконання

### Опис

```methodsynopsis
oci_parse(resource $connection, string $sql): resource|false
```

Готує `sql` до виконання, використовуючи з'єднання `connection` і повертає ідентифікатор виразу, який може бути використаний далі функціями[ocibindбname()](function.oci-bind-by-name.html)[ociexecute()](function.oci-execute.html) та іншими.

Ідентифікатори виразів можуть бути звільнені функцією [ocifreestatement()](function.oci-free-statement.html) або встановленням змінної в **`null`**

### Список параметрів

`connection`

Ідентифікатор з'єднання Oracle, отриманий із функцій [ociconnect()](function.oci-connect.html) [ocipconnect()](function.oci-pconnect.html) або [ocinewconnect()](function.oci-new-connect.html)

`sql`

Запит SQL або PL/SQL.

SQL-запити *не повинні* закінчуватися точкою з комою (";"). PL/SQL-запити *повинні* закінчуватися точкою з комою (";").

### Значення, що повертаються

Повертає дескриптор виразу у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ociparse()** із SQL-запитами**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

// Парсинг запроса. Обратите внимание на отсутствие точки запятой в конце SQL-запроса
$stid = oci_parse($conn, 'SELECT * FROM employees');
oci_execute($stid);

echo "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

?>
```

**Приклад #2 Приклад використання **ociparse()** з PL/SQL-запитами**

```php
<?php

/*
  Перед запуском PHP-скрипта, создайте хранимую процедуру в
  SQL*Plus или SQL Developer:

  CREATE OR REPLACE PROCEDURE myproc(p1 IN NUMBER, p2 OUT NUMBER) AS
  BEGIN
      p2 := p1 * 2;
  END;

*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$p1 = 8;

// При парсинге PL/SQL запросов необходимо наличие точки с запятой в конце строки
$stid = oci_parse($conn, 'begin myproc(:p1, :p2); end;');
oci_bind_by_name($stid, ':p1', $p1);
oci_bind_by_name($stid, ':p2', $p2, 40);

oci_execute($stid);

print "$p2\n";   // prints 16

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> Ця функція *не перевіряє* синтаксис запиту `sql`. Єдиний спосіб перевірити правильність SQL чи PL/SQL-запиту `sql` - це здійснити його.

### Дивіться також

-   [ociexecute()](function.oci-execute.html) - Виконує підготовлений вираз
-   [ocifreestatement()](function.oci-free-statement.html) - Звільняє ресурси, які займає курсор або SQL-вираз.
