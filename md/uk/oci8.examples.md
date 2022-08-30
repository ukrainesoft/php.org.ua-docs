Приклади

-   [« Обумовлені константи](oci8.constants.html)
    
-   [Работа с соединениями OCI8 и Connection Pooling »](oci8.connection.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8](book.oci8.html)
    
-   Приклади
    

# Приклади

Ці приклади виконуються під користувачем `HR`, Який є зразком з "Human Resources" схеми, що поставляється разом з базою даних Oracle. Можливо, потрібно розблокувати цей обліковий запис і перевстановити для нього пароль, щоб використовувати його.

Приклади підключаються до бази даних `XE` на вашому комп'ютері. Ви можете замінити рядки з підключенням для використання баз даних.

**Приклад #1 Простий запит**

Даний приклад показує запит та результат. Вирази в OCI8 використовують послідовність з кроків підготовка-виконання-вибірка.

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

// Подготовка выражения
$stid = oci_parse($conn, 'SELECT * FROM departments');
if (!$stid) {
    $e = oci_error($conn);
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

// Выполним логику запроса
$r = oci_execute($stid);
if (!$r) {
    $e = oci_error($stid);
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

// Получим результат запроса
print "<table border='1'>\n";
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    print "<tr>\n";
    foreach ($row as $item) {
        print "    <td>" . ($item !== null ? htmlentities($item, ENT_QUOTES) : "") . "</td>\n";
    }
    print "</tr>\n";
}
print "</table>\n";

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Вставка з використанням прив'язаних змінних**

Прив'язування змінних підвищують продуктивність рахунок повторного використання контексту запиту і кешування. Також вони підвищують безпеку, блокуючи деякі типи SQL-ін'єкцій.

```php
<?php

// Создайте таблицу перед выполнением:
//   CREATE TABLE MYTABLE (mid NUMBER, myd VARCHAR2(20));

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'INSERT INTO MYTABLE (mid, myd) VALUES(:myid, :mydata)');

$id = 60;
$data = 'Some data';

oci_bind_by_name($stid, ':myid', $id);
oci_bind_by_name($stid, ':mydata', $data);

$r = oci_execute($stid);  // выполнение и фиксация

if ($r) {
    print "Была вставлена одна строка";
}

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 Прив'язка у WHERE виразі запиту**

Приклад одиничного прив'язування скаляра.

```php
<?php

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$sql = 'SELECT last_name FROM employees WHERE department_id = :didbv ORDER BY last_name';
$stid = oci_parse($conn, $sql);
$didbv = 60;
oci_bind_by_name($stid, ':didbv', $didbv);
oci_execute($stid);
while (($row = oci_fetch_array($stid, OCI_ASSOC)) != false) {
    echo $row['LAST_NAME'] ."<br>\n";
}

// Выведет
//    Austin
//    Ernst
//    Hunold
//    Lorentz
//    Pataballa

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #4 Вставлення даних у поле типу CLOB**

Використовуйте довгі двійкові об'єкти (BLOB) або довгі символьні об'єкти (CLOB). Цей приклад використовує тип даних CLOB.

```php
<?php

// Создайте таблицу перед выполнением:
//     CREATE TABLE MYTABLE (mykey NUMBER, myclob CLOB);

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$mykey = 12343;  // произвольный ключ для данного примера;

$sql = "INSERT INTO mytable (mykey, myclob)
        VALUES (:mykey, EMPTY_CLOB())
        RETURNING myclob INTO :myclob";

$stid = oci_parse($conn, $sql);
$clob = oci_new_descriptor($conn, OCI_D_LOB);
oci_bind_by_name($stid, ":mykey", $mykey, 5);
oci_bind_by_name($stid, ":myclob", $clob, -1, OCI_B_CLOB);
oci_execute($stid, OCI_NO_AUTO_COMMIT); // используйте OCI_DEFAULT для PHP <= 5.3.1
$clob->save("A very long string");

oci_commit($conn);

// Получение CLOB данных

$query = 'SELECT myclob FROM mytable WHERE mykey = :mykey';

$stid = oci_parse ($conn, $query);
oci_bind_by_name($stid, ":mykey", $mykey, 5);
oci_execute($stid);

print '<table border="1">';
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_LOBS)) {
    print '<tr><td>'.$row['MYCLOB'].'</td></tr>';
    // В цикле, очищение больших переменных перед повторным получением данных, уменьшает пиковое потребление памяти PHP
    unset($row);
}
print '</table>';

?>
```

**Приклад #5 Використання PL/SQL процедур, що зберігаються**

Ви повинні прив'язувати змінну для кожного значення, що повертається, і опціонально для кожного аргументу функції.

```php
<?php

/*
  До выполнения PHP-скрипта сойздайте хранимую процедуру в
  SQL*Plus или SQL Developer:

  CREATE OR REPLACE FUNCTION myfunc(p IN NUMBER) RETURN NUMBER AS
  BEGIN
      RETURN p * 3;
  END;

*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$p = 8;

$stid = oci_parse($conn, 'begin :r := myfunc(:p); end;');
oci_bind_by_name($stid, ':p', $p);
oci_bind_by_name($stid, ':r', $r, 40);

oci_execute($stid);

print "$r\n";   // выведет 24

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #6 Використання PL/SQL процедур, що зберігаються**

При використанні процедур, що зберігаються, бажано прив'язувати змінні до кожного аргументу.

```php
<?php

/*
  До выполнения PHP-скрипта сойздайте хранимую процедуру в
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

$stid = oci_parse($conn, 'begin myproc(:p1, :p2); end;');
oci_bind_by_name($stid, ':p1', $p1);
oci_bind_by_name($stid, ':p2', $p2, 40);

oci_execute($stid);

print "$p2\n";   // выведет 16

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #7 Виклик PL/SQL процедур, що повертають `REF CURSOR`**

Кожне значення, що повертається із запиту є `REF CURSOR`

```php
<?php
/*
  Создайте PL/SQL хранимую процедуру:

  CREATE OR REPLACE FUNCTION myfunc(p1 IN NUMBER) RETURN SYS_REFCURSOR AS
      rc SYS_REFCURSOR;
  BEGIN
      OPEN rc FOR SELECT city FROM locations WHERE ROWNUM < p1;
      RETURN rc;
  END;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');

$stid = oci_parse($conn, 'SELECT myfunc(5) AS mfrc FROM dual');
oci_execute($stid);

echo "<table border='1'>\n";
while (($row = oci_fetch_array($stid, OCI_ASSOC))) {
    echo "<tr>\n";
    $rc = $row['MFRC'];
    oci_execute($rc);  // возвращает значение поля из запроса в виде указателя
    while (($rc_row = oci_fetch_array($rc, OCI_ASSOC))) {
        echo "    <td>" . $rc_row['CITY'] . "</td>\n";
    }
    oci_free_statement($rc);
    echo "</tr>\n";
}
echo "</table>\n";

// Выведет:
//   Beijing
//   Bern
//   Bombay
//   Geneva

oci_free_statement($stid);
oci_close($conn);

?>
```