---
navigation:
  - function.oci-free-statement.md: « oci\_free\_statement
  - function.oci-lob-copy.md: oci\_lob\_copy »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_get\_implicit\_resultset
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_get\_implicit\_resultset

(PHP 5 >= 5.6.0, PHP 7, PHP 8, PECL OCI8 >= 2.0.0)

oci\_get\_implicit\_resultset — Повертає наступний ресурс дочірнього запиту з батьківського запиту, що має неявні результуючі набори Oracle Database

### Опис

```methodsynopsis
oci_get_implicit_resultset(resource $statement): resource|false
```

Використовується для вибірки послідовних наборів результатів запиту після виконання збереженого або анонімного блоку Oracle PL/SQL, коли цей блок повертає результати запиту Oracle Database 12 (або новіше) за допомогою функції PL/SQL *DBMS\_SQL.RETURN\_RESULT*. Це дозволить блокам PL/SQL повертати результати запиту.

Дочірній запит може бути використаний з будь-якою функцією OCI8: [oci\_fetch()](function.oci-fetch.md) [oci\_fetch\_all()](function.oci-fetch-all.md) [oci\_fetch\_array()](function.oci-fetch-array.md) [oci\_fetch\_object()](function.oci-fetch-object.md) [oci\_fetch\_assoc()](function.oci-fetch-assoc.md) або [oci\_fetch\_row()](function.oci-fetch-row.md)

Дочірній запит успадковує батьківське значення передвиборки, або можна вказати його за допомогою [oci\_set\_prefetch()](function.oci-set-prefetch.md)

### Список параметрів

`statement`

Коректний ідентифікатор запиту OCI8, створений за допомогою [oci\_parse()](function.oci-parse.md) та запущений за допомогою [oci\_execute()](function.oci-execute.md). Ідентифікатор запиту може бути, а може і не бути пов'язаний із SQL-запитом, який повертає неявні результуючі набори (Implicit Result Set).

### Значення, що повертаються

Возвращает обработчик запроса для следующего доступного для`statement` дочірній запит. Повертає **`false`** якщо такого немає або всі дочірні запити вже повернуто попередніми викликами **oci\_get\_implicit\_resultset()**

### Приклади

**Приклад #1 Вилучення неявних результуючих наборів у циклі**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/pdborcl');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'DECLARE
            c1 SYS_REFCURSOR;
        BEGIN
           OPEN c1 FOR SELECT city, postal_code FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
           OPEN c1 FOR SELECT country_id FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
        END;';

$stid = oci_parse($conn, $sql);
oci_execute($stid);

while (($stid_c = oci_get_implicit_resultset($stid))) {
    echo "<h2>Новый неявный результирующий набор:</h2>\n";
    echo "<table>\n";
    while (($row = oci_fetch_array($stid_c, OCI_ASSOC+OCI_RETURN_NULLS)) != false) {
        echo "<tr>\n";
        foreach ($row as $item) {
            echo "  <td>".($item!==null?htmlentities($item, ENT_QUOTES|ENT_SUBSTITUTE):"")."</td>\n";
        }
        echo "</tr>\n";
    }
    echo "</table>\n";
}

// Вывод:
//    Новый неявный результирующий набор:
//     Beijing 190518
//     Bern    3095
//     Bombay  490231
//    New Implicit Result Set:
//     CN
//     CH
//     IN

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Вилучення обробників дочірніх запитів в індивідуальному порядку**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/pdborcl');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'DECLARE
            c1 SYS_REFCURSOR;
        BEGIN
           OPEN c1 FOR SELECT city, postal_code FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
           OPEN c1 FOR SELECT country_id FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
        END;';

$stid = oci_parse($conn, $sql);
oci_execute($stid);

$stid_1 = oci_get_implicit_resultset($stid);
$stid_2 = oci_get_implicit_resultset($stid);

$row = oci_fetch_array($stid_1, OCI_ASSOC+OCI_RETURN_NULLS);
var_dump($row);
$row = oci_fetch_array($stid_2, OCI_ASSOC+OCI_RETURN_NULLS);
var_dump($row);
$row = oci_fetch_array($stid_1, OCI_ASSOC+OCI_RETURN_NULLS);
var_dump($row);
$row = oci_fetch_array($stid_2, OCI_ASSOC+OCI_RETURN_NULLS);
var_dump($row);

// Вывод:
//    array(2) {
//      ["CITY"]=>
//      string(7) "Beijing"
//      ["POSTAL_CODE"]=>
//      string(6) "190518"
//    }
//    array(1) {
//      ["COUNTRY_ID"]=>
//      string(2) "CN"
//    }
//    array(2) {
//      ["CITY"]=>
//      string(4) "Bern"
//      ["POSTAL_CODE"]=>
//      string(4) "3095"
//    }
//    array(1) {
//      ["COUNTRY_ID"]=>
//      string(2) "CH"
//    }

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 Явна вказівка ​​величини передвиборки**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/pdborcl');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'DECLARE
            c1 SYS_REFCURSOR;
        BEGIN
           OPEN c1 FOR SELECT city, postal_code FROM locations ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
        END;';

$stid = oci_parse($conn, $sql);
oci_execute($stid);

$stid_c = oci_get_implicit_resultset($stid);
oci_set_prefetch($stid_c, 200);   // Устанавливаем величину предвыборки до того как начинаем извлекать пезультаты из дочернего запроса
echo "<table>\n";
while (($row = oci_fetch_array($stid_c, OCI_ASSOC+OCI_RETURN_NULLS)) != false) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "  <td>".($item!==null?htmlentities($item, ENT_QUOTES|ENT_SUBSTITUTE):"")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #4 Приклад неявного результуючого набору без використання **oci\_get\_implicit\_resultset()****

Усі результати всіх запитів повертаються послідовно.

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/pdborcl');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'DECLARE
            c1 SYS_REFCURSOR;
        BEGIN
           OPEN c1 FOR SELECT city, postal_code FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
           OPEN c1 FOR SELECT country_id FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
        END;';

$stid = oci_parse($conn, $sql);
oci_execute($stid);

// Обратите внимание: oci_fetch_all and oci_fetch() нельзя использовать таким образом
echo "<table>\n";
while (($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) != false) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "  <td>".($item!==null?htmlentities($item, ENT_QUOTES|ENT_SUBSTITUTE):"")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

// Вывод:
//    Beijing 190518
//    Bern 3095
//    Bombay 490231
//    CN
//    CH
//    IN

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження** :
> 
> Для запитів, що повертають велику кількість рядів, продуктивність може бути значно збільшена за допомогою збільшення значення опції [oci8.default\_prefetch](oci8.configuration.md#ini.oci8.default-prefetch)или использования[oci\_set\_prefetch()](function.oci-set-prefetch.md)
