---
navigation:
  - function.oci-bind-array-by-name.html: « ocibindarrayбname
  - function.oci-cancel.html: ocicancel »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocibindбname
---
# ocibindбname

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocibindбname — Прикріплює змінну PHP до відповідної мітки у SQL-вираженні

### Опис

```methodsynopsis
oci_bind_by_name(    resource $statement,    string $param,    mixed &$var,    int $max_length = -1,    int $type = 0): bool
```

Прикріплює змінну `var` до мітки `param`. Таке прикріплення дозволяє підвищити продуктивність та уникнути SQL-ін'єкцій.

Прикріплення змінної дозволяє базі даних повторно використовувати кешовані контекстні вирази від попередніх запитів, навіть якщо вони спочатку були запущені іншим користувачем чи процесом. Це також знижує ризик ін'єкцій SQL, оскільки дані в такому випадку ніколи не розглядаються як інструкції SQL. Дані не потрібно екранувати або укладати в лапки.

Прикріплені PHP-змінні можуть бути змінені та знову виконані без необхідності повторного оброблення запиту або повторного прикріплення.

У Oracle прикріплення змінних зазвичай поділяють на `IN` (прикріплює значення, що передаються в базу даних) та `OUT` (Прикріплює значення, що повертаються PHP). Змінна може бути одночасно `IN` і `OUT`. Незалежно від цього характер прикріплення змінних буде визначено під час виконання.

Необхідно вказати `max_length` при використанні `OUT`прив'язки, що дозволяє PHP зарезервувати більше пам'яті для зберігання значення, що повертається

Для `IN`рекомендується також вказати параметр прив'язки `max_length`, якщо вираз виконується кілька разів із різними значеннями PHP-змінної. В іншому випадку Oracle може урізати розмір даних до розміру початкового значення змінної PHP. Якщо максимальна довжина невідома, рекомендується викликати **ocibindбname()** перед кожним викликом [ociexecute()](function.oci-execute.md). Прикріплення невиправдано великої змінної вплине процес збереження бази даних.

Вигляд прикріплення вказує Oracle як працювати з пам'яттю під час читання даних. Для `IN`прикріплення адрес у пам'яті повинен містити допустимі дані під час виклику [ociexecute()](function.oci-execute.md). Це означає, що значення змінної має бути у пам'яті під час виконання. Якщо це не так, можливі некоректні результати або помилки на кшталт "ORA-01460: unimplemented or unreasonable conversion requested" (запитані нездійсненні або некоректні перетворення) `OUT`Прикріплення основною ознакою є встановлення значення змінної PHP.

Для виразу, що багаторазово виконується, прив'язка одних і тих же значень може зменшити можливості оптимізатора Oracle з вироблення найкращого варіанту виконання інструкції. Тривале прикріплення виразів, які рідко виконуються, може також принести користі. Тим не менш, в обох випадках, прикріплення є більш безпечним, ніж конкатенація рядка запиту та неперевірених даних користувача.

### Список параметрів

`statement`

Допустимий ідентифікатор виразу OCI8.

`param`

Мітка з префіксом у вигляді двокрапки, що використовується у виразі. Двокрапка опціонально в `param`. Oracle не використовує питання для позначок.

`var`

Змінна PHP, асоційована з `param`

`max_length`

Встановлює максимальний розмір даних. Якщо вказати -1, функція буде використовувати поточний розмір змінної `var` як максимальне. При цьому змінна `var` має існувати та містити дані під час виклику **ocibindбname()**

`type`

Тип даних, до якого Oracle наводитиме значення. За замовчуванням `type` має значення **`SQLT_CHR`**. Oracle наводить дані від даного типу до типу поля (або типу змінної PL/SQL), якщо це можливо.

Якщо необхідно прикріпити змінну абстрактного типу (LOB/ROWID/BFILE), слід попередньо використовувати [ocinewdescriptor()](function.oci-new-descriptor.md). Параметр `length` не використовується для абстрактних типів і повинен бути встановлений -1.

Допустимі значення параметра `type`

-   **`SQLT_BFILEE`** або **`OCI_B_BFILE`** - для BFILE-об'єктів;
    
-   **`SQLT_CFILEE`** або **`OCI_B_CFILEE`** - для CFILE-об'єктів;
    
-   **`SQLT_CLOB`** або **`OCI_B_CLOB`** - для CLOB-об'єктів;
    
-   **`SQLT_BLOB`** або **`OCI_B_BLOB`** - для BLOB-об'єктів;
    
-   **`SQLT_RDD`** або **`OCI_B_ROWID`** - для ROWID-об'єктів;
    
-   **`SQLT_NTY`** або **`OCI_B_NTY`** - для іменованих типів дати;
    
-   **`SQLT_INT`** або **`OCI_B_INT`** - для цілих чисел;
    
-   **`SQLT_CHR`** - для символів VARCHAR;
    
-   **`SQLT_BIN`** або **`OCI_B_BIN`** - для RAW-полів;
    
-   **`SQLT_LNG`** - для LONG-полів;
    
-   **`SQLT_LBI`** - для LONG RAW полів;
    
-   **`SQLT_RSET`** - для курсорів, створених функцією [ocinewcursor()](function.oci-new-cursor.md)
    
-   **`SQLT_BOL`** або **`OCI_B_BOL`** - для PL/SQL BOOLEAN (Потрібен OCI8 2.0.7 та Oracle Database 12c)
    

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Додавання даних із використанням **ocibindбname()****

```php
<?php

// Создание таблицы:
//   CREATE TABLE mytab (id NUMBER, text VARCHAR2(40));

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn,"INSERT INTO mytab (id, text) VALUES(:id_bv, :text_bv)");

$id = 1;
$text = "Data to insert     ";
oci_bind_by_name($stid, ":id_bv", $id);
oci_bind_by_name($stid, ":text_bv", $text);
oci_execute($stid);

// В таблице содержится: 1, 'Data to insert     '

?>
```

**Приклад #2 Одна прив'язка для багаторазового використання**

```php
<?php

// Создание таблицы:
//   CREATE TABLE mytab (id NUMBER);

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$a = array(1,3,5,7,11);  // данные для вставки

$stid = oci_parse($conn, 'INSERT INTO mytab (id) VALUES (:bv)');
oci_bind_by_name($stid, ':bv', $v, 20);
foreach ($a as $v) {
    $r = oci_execute($stid, OCI_DEFAULT);  // не использовать автоматическое завершение транзакции
}
oci_commit($conn); // завершение транзакции

// Таблица содержит пять записей: 1, 3, 5, 7, 11

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 Прикріплення у циклі `foreach`**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$sql = 'SELECT * FROM departments WHERE department_name = :dname AND location_id = :loc';
$stid = oci_parse($conn, $sql);

$ba = array(':dname' => 'IT Support', ':loc' => 1700);

foreach ($ba as $key => $val) {

    // oci_bind_by_name($stid, $key, $val) не работает,
    // потому что прикрепляет каждое значение в одно место: $val
    // Вместо этого следует указывать конкретное место: $ba[$key]
    oci_bind_by_name($stid, $key, $ba[$key]);
}

oci_execute($stid);
$row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS);
foreach ($row as $item) {
    print $item."<br>\n";
}

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #4 Прикріплення до виразу WHERE**

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

// Выводом будет
//    Austin
//    Ernst
//    Hunold
//    Lorentz
//    Pataballa

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #5 Прикріплення до виразу LIKE**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

// Поиск всех городов, начинающихся на 'South'
$stid = oci_parse($conn, "SELECT city FROM locations WHERE city LIKE :bv");
$city = 'South%';  // '%' - это знак шаблона SQL
oci_bind_by_name($stid, ":bv", $city);
oci_execute($stid);
oci_fetch_all($stid, $res);

foreach ($res['CITY'] as $c) {
    print $c . "<br>\n";
}
// Выводом будет:
//   South Brunswick
//   South San Francisco
//   Southlake

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #6 Прикріплення до виразу REGEXPLIKE**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

// Поиск названий городов, содержащих 'ing'
$stid = oci_parse($conn, "SELECT city FROM locations WHERE REGEXP_LIKE(city, :bv)");
$city = '.*ing.*';
oci_bind_by_name($stid, ":bv", $city);
oci_execute($stid);
oci_fetch_all($stid, $res);

foreach ($res['CITY'] as $c) {
    print $c . "<br>\n";
}
// Выводом будет:
//   Beijing
//   Singapore

oci_free_statement($stid);
oci_close($conn);

?>
```

Для невеликої, фіксованої кількості умов у виразі IN використовуються індивідуальні імена змінних. Невідомі значення під час виконання можуть бути встановлені в NULL. Це дозволяє використовувати один вираз декільком користувачам, що підвищує ефективність кешування Oracle DB.

**Приклад #7 Прикріплення кількох значень у вираз IN**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$sql = 'SELECT last_name FROM employees WHERE employee_id in (:e1, :e2, :e3)';
$stid = oci_parse($conn, $sql);
$mye1 = 103;
$mye2 = 104;
$mye3 = NULL; // притворимся, что не получили это значение
oci_bind_by_name($stid, ':e1', $mye1);
oci_bind_by_name($stid, ':e2', $mye2);
oci_bind_by_name($stid, ':e3', $mye3);
oci_execute($stid);
oci_fetch_all($stid, $res);
foreach ($res['LAST_NAME'] as $name) {
    print $name ."<br>\n";
}

// Выводом будет:
//   Ernst
//   Hunold

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #8 Прикріплення ROWID, що повертається запитом**

```php
<?php

// Создадим и наполним таблицу:
//   CREATE TABLE mytab (id NUMBER, salary NUMBER, name VARCHAR2(40));
//   INSERT INTO mytab (id, salary, name) VALUES (1, 100, 'Chris');
//   COMMIT;

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT ROWID, name FROM mytab WHERE id = :id_bv FOR UPDATE');
$id = 1;
oci_bind_by_name($stid, ':id_bv', $id);
oci_execute($stid);
$row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS);
$rid = $row['ROWID'];
$name = $row['NAME'];

// Переведём имя в верхний регистр и зафиксируем изменения
$name = strtoupper($name);
$stid = oci_parse($conn, 'UPDATE mytab SET name = :n_bv WHERE ROWID = :r_bv');
oci_bind_by_name($stid, ':n_bv', $name);
oci_bind_by_name($stid, ':r_bv', $rid, -1, OCI_B_ROWID);
oci_execute($stid);

// Теперь таблица содержит: 1, 100, CHRIS

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #9 OUT-прикріплення ROWID, яке повертається при INSERT**

```php
<?php

// В данном примере добавляется запись с идентификатором и именем,
// после чего увеличивается заработная плата
// Создание таблицы:
//   CREATE TABLE mytab (id NUMBER, salary NUMBER, name VARCHAR2(40));
//
// На основе собственных ROWID на примере thies[at]thieso.net (980221)

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$sql = "INSERT INTO mytab (id, name) VALUES(:id_bv, :name_bv)
        RETURNING ROWID INTO :rid";

$ins_stid = oci_parse($conn, $sql);

$rowid = oci_new_descriptor($conn, OCI_D_ROWID);
oci_bind_by_name($ins_stid, ":id_bv",   $id,    10);
oci_bind_by_name($ins_stid, ":name_bv", $name,  32);
oci_bind_by_name($ins_stid, ":rid",     $rowid, -1, OCI_B_ROWID);

$sql = "UPDATE mytab SET salary = :salary WHERE ROWID = :rid";
$upd_stid = oci_parse($conn, $sql);
oci_bind_by_name($upd_stid, ":rid", $rowid, -1, OCI_B_ROWID);
oci_bind_by_name($upd_stid, ":salary", $salary,   32);

// идентификаторы и имена для вставки
$data = array(1111 => "Larry",
              2222 => "Bill",
              3333 => "Jim");

// Заработная плата для каждого сотрудника
$salary = 10000;

// Вставка и немедленное обновление каждой строки
foreach ($data as $id => $name) {
    oci_execute($ins_stid);
    oci_execute($upd_stid);
}

$rowid->free();
oci_free_statement($upd_stid);
oci_free_statement($ins_stid);

// Показать новые записи
$stid = oci_parse($conn, "SELECT * FROM mytab");
oci_execute($stid);
while ($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) {
    var_dump($row);
}

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #10 Прикріплення для PL/SQL, що зберігається.**

```php
<?php

//  Перед запуском PHP-сценария, создайте хранимую функцию в
//  SQL*Plus или SQL Developer:
//
//  CREATE OR REPLACE FUNCTION myfunc(p IN NUMBER) RETURN NUMBER AS
//  BEGIN
//      RETURN p * 3;
//  END;

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

$p = 8;

$stid = oci_parse($conn, 'begin :r := myfunc(:p); end;');
oci_bind_by_name($stid, ':p', $p);

// Возвращаемое значение OUT-прикреплено. По умолчаннию типом данных будет строка.
// Прикрепление со значением 40 означает, что будет возвращено 40 символов.
oci_bind_by_name($stid, ':r', $r, 40);

oci_execute($stid);

print "$r\n";   // выведет 24

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #11 Прикріплення параметрів для PL/SQL збереженої процедури**

```php
<?php

//  Перед запуском PHP-сценария, создайте хранимую процедуру в
//  SQL*Plus или SQL Developer:
//
//  CREATE OR REPLACE PROCEDURE myproc(p1 IN NUMBER, p2 OUT NUMBER) AS
//  BEGIN
//      p2 := p1 * 2;
//  END;

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

$p1 = 8;

$stid = oci_parse($conn, 'begin myproc(:p1, :p2); end;');
oci_bind_by_name($stid, ':p1', $p1);

// Второй параметр процедуры OUT-прикреплён. По умолчаннию типом данных будет строка.
// Прикрепление со значением 40 означает, что будет возвращено 40 символов.
oci_bind_by_name($stid, ':p2', $p2, 40);

oci_execute($stid);

print "$p2\n";   // выведет 16

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #12 Прикріплення об'єкта CLOB**

```php
<?php

// Перед запуском создаём таблицу:
//     CREATE TABLE mytab (mykey NUMBER, myclob CLOB);

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

$mykey = 12343;  // произвольный ключ для примера

$sql = "INSERT INTO mytab (mykey, myclob)
        VALUES (:mykey, EMPTY_CLOB())
        RETURNING myclob INTO :myclob";

$stid = oci_parse($conn, $sql);
$clob = oci_new_descriptor($conn, OCI_D_LOB);
oci_bind_by_name($stid, ":mykey", $mykey, 5);
oci_bind_by_name($stid, ":myclob", $clob, -1, OCI_B_CLOB);
oci_execute($stid, OCI_DEFAULT);
$clob->save("A very long string");

oci_commit($conn);

// Получение CLOB-данных

$query = 'SELECT myclob FROM mytab WHERE mykey = :mykey';

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

**Приклад #13 Прикріплення PL/SQL BOOLEAN**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message']), E_USER_ERROR);
}

$plsql =
  "begin
    :output1 := true;
    :output2 := false;
   end;";

$s = oci_parse($c, $plsql);
oci_bind_by_name($s, ':output1', $output1, -1, OCI_B_BOL);
oci_bind_by_name($s, ':output2', $output2, -1, OCI_B_BOL);
oci_execute($s);
var_dump($output1);  // true
var_dump($output2);  // false

?>
```

### Примітки

**Увага**

Не використовуйте [addslashes()](function.addslashes.md) одночасно з **ocibindбname()**, так як лапок бути не повинно. Всі зазначені лапки будуть записані до бази даних, тому що **ocibindбname()** вставляє дані дослівно і не видаляє лапки або символи екранування.

> **Зауваження**
> 
> Якщо прикріплюється рядок до `CHAR`полю у виразі `WHERE`, пам'ятайте, що Oracle використовує для порівняння значення `CHAR`, доповнені пробілами. Змінна PHP повинна бути доповнена пробілами до того ж розміру, що і поле, щоб вираз `WHERE` виконувалося правильно.

> **Зауваження**
> 
> Змінна PHP `var` є посиланням. Деякі види циклів можуть працювати не так, як очікується:
> 
> ```php
> <?php
> foreach ($myarray as $key => $value)  {
>     oci_bind_by_name($stid, $key, $value);
> }
> ?>
> ```
> 
> У цьому випадку кожен ключ прикріплюється до $value, тому всі прикріплені змінні вказують на значення останньої ітерації циклу. Натомість слід використовувати:
> 
> ```php
> <?php
> foreach ($myarray as $key => $value) {
>     oci_bind_by_name($stid, $key, $myarray[$key]);
> }
> ?>
> ```

### Дивіться також

-   [ocibindarrayбname()](function.oci-bind-array-by-name.md) - Пов'язує PHP масив з масивом Oracle PL/SQL
-   [ociparse()](function.oci-parse.md) - готує запит до виконання
