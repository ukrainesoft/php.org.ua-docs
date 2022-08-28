Повертає наступний рядок з результату запиту у вигляді асоціативного чи нумерованого масиву

-   [« oci\_fetch\_all](function.oci-fetch-all.html)
    
-   [oci\_fetch\_assoc »](function.oci-fetch-assoc.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Повертає наступний рядок з результату запиту у вигляді асоціативного чи нумерованого масиву
    

# ocifetcharray

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifetcharray - Повертає наступний рядок з результату запиту у вигляді асоціативного або нумерованого масиву

### Опис

```methodsynopsis
oci_fetch_array(resource $statement, int $mode = OCI_BOTH | OCI_RETURN_NULLS): array|false
```

Повертає масив, що містить наступний рядок результату запиту. Кожен елемент масиву відповідає одному полю рядка. Ця функція зазвичай викликається в циклі, доки вона не поверне **`false`**що вказує на відсутність наступних рядків.

Якщо `statement` відповідає PL/SQL блоку, що повертається Oracle Database Implicit Result Sets, тоді буде послідовно вилучено ряди з усіх наборів. Якщо `statement` повертається з [oci\_get\_implicit\_resultset()](function.oci-get-implicit-resultset.html)тоді повернеться лише частина рядів для одного дочірнього запиту.

Для отримання детальнішої інформації щодо відображення типів даних модуля OCI8 зверніться до [типам данных, поддерживаемых драйвером](oci8.datatypes.html)

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.html) та виконаний функцією [oci\_execute()](function.oci-execute.html), або ідентифікатор виразу `REF CURSOR`

Також може бути ідентифікатором, що повертається функцією [oci\_get\_implicit\_resultset()](function.oci-get-implicit-resultset.html)

`mode`

Необов'язковий другий параметр може складатися з будь-якої комбінації наступних констант:

****ocifetcharray()** Modes**

| Константа | Описание |
| --- | --- |
| **`OCI_BOTH`** | Повертає масив як з асоціативними та числовими індексами. Ця константа те саме, що й **`OCI_ASSOC`** **`OCI_NUM`**, і вона використовується за замовчуванням. |
| **`OCI_ASSOC`** | Повертає асоціативний масив. |
| **`OCI_NUM`** | Повертає нумерований масив. |
| **`OCI_RETURN_NULLS`** | Створює елементи для рівних полів **`null`**. Значення елемента дорівнюватиме PHP **`null`** |
| **`OCI_RETURN_LOBS`** | Повертає вміст полів типу LOB замість LOB покажчика. |

За замовчуванням `mode` дорівнює **`OCI_BOTH`**

Використовуйте оператор додавання "+", щоб вказати більше одного режиму.

### Значення, що повертаються

Повертає масив з асоціативними та/або числовими ключами. Якщо більше немає рядків у `statement`, то повертається **`false`**

За замовчуванням поля `LOB` повертаються як покажчики LOB.

Поля типу `DATE` повертаються у форматі рядків, що відповідає поточному формату дати. Формат за промовчанням може бути змінений за допомогою змінних оточення Oracle, таких як `NLS_LANG`, або попереднім виконанням команди `ALTER SESSION SET NLS_DATE_FORMAT`

Регістронезалежні (за замовчуванням у Oracle) імена полів матимуть асоціативні індекси у верхньому регістрі в результуючому масиві. Регістрозалежні імена полів матимуть індекси з тими самими регістрами символів, як і саме поле. Використовуйте [var\_dump()](function.var-dump.html) для результуючого масиву, щоб перевірити відповідність регістрів символів кожному за запиту.

Ім'я таблиці не входить до асоціативного індексу. Якщо ваш запит містить два різні поля з однаковим ім'ям, використовуйте **`OCI_NUM`** або додайте аліас для поля у запит, щоб імена стали унікальними (дивіться приклад #7). Інакше буде повернуто лише одне поле.

### Приклади

**Приклад #1 **ocifetcharray()** з **`OCI_BOTH`****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT department_id, department_name FROM departments');
oci_execute($stid);

while (($row = oci_fetch_array($stid, OCI_BOTH))) {
    // Используйте название полей в верхнем регистре для ассоциативных индексов
    echo $row[0] . " и " . $row['DEPARTMENT_ID']   . " идентичны<br>\n";
    echo $row[1] . " и " . $row['DEPARTMENT_NAME'] . " идентичны<br>\n";
}

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 **ocifetcharray()** з **`OCI_NUM`****

```php
<?php

/*
  Перед выполнением создайте таблицу:
      CREATE TABLE mytab (id NUMBER, description CLOB);
      INSERT INTO mytab (id, description) values (1, 'A very long string');
      COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, description FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_array($stid, OCI_NUM)) != false) {
    echo $row[0] . "<br>\n";
    echo $row[1]->read(11) . "<br>\n"; // это выведет первые 11 байт DESCRIPTION
}

// Выведет:
//    1
//    A very long

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 **ocifetcharray()** з **`OCI_ASSOC`****

```php
<?php

/*
  Перед выполнением создайте таблицу:
      CREATE TABLE mytab (id NUMBER, description CLOB);
      INSERT INTO mytab (id, description) values (1, 'A very long string');
      COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, description FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_array($stid, OCI_ASSOC)) != false) {
    echo $row['ID'] . "<br>\n";
    echo $row['DESCRIPTION']->read(11) . "<br>\n"; // это выведет первые 11 байт DESCRIPTION
}

// Выведет:
//    1
//    A very long

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #4 **ocifetcharray()** з **`OCI_RETURN_NULLS`****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT 1, null FROM dual');
oci_execute($stid);
while (($row = oci_fetch_array ($stid, OCI_ASSOC)) != false) { // Игнорирует NULL значения
    var_dump($row);
}

/*
Вышеуказанный код выведет:
  array(1) {
    [1]=>
    string(1) "1"
  }
*/

$stid = oci_parse($conn, 'SELECT 1, null FROM dual');
oci_execute($stid);
while (($row = oci_fetch_array ($stid, OCI_ASSOC+OCI_RETURN_NULLS)) != false) { // Получает NULL значения
    var_dump($row);
}

/*
Вышеуказанный код выведет:
  array(2) {
    [1]=>
    string(1) "1"
    ["NULL"]=>
    NULL
  }
*/

?>
```

**Приклад #5 **ocifetcharray()** з **`OCI_RETURN_LOBS`****

```php
<?php

/*
  Перед выполнением создайте таблицу:
      CREATE TABLE mytab (id NUMBER, description CLOB);
      INSERT INTO mytab (id, description) values (1, 'A very long string');
      COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, description FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_LOBS))) {
    echo $row['ID'] . "<br>\n";
    echo $row['DESCRIPTION'] . "<br>\n"; // содержит весь DESCRIPTION
    // В цикле, очищение больших переменных перед повторным получением данных, уменьшает пиковое потребление памяти PHP
    unset($row);
}

// Выведет:
//    1
//    A very long string

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #6 **ocifetcharray()** з реєстрозалежними назвами полів**

```php
<?php

/*
   Перед выполнением создайте таблицу:
      CREATE TABLE mytab ("Name" VARCHAR2(20), city VARCHAR2(20));
      INSERT INTO mytab ("Name", city) values ('Chris', 'Melbourne');
      COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'select * from mytab');
oci_execute($stid);
$row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS);

// Так как 'Name' было создан как регистрозависимое поле, то
// те же регисты символов используются для индексов массива.
// Тем не менее для 'CITY' должен использоваться индекс в верхнем регистре.
print $row['Name'] . "<br>\n";   //  выведет Chris
print $row['CITY'] . "<br>\n";   //  выведет Melbourne

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #7 **ocifetcharray()** з полями з однаковими назвами**

```php
<?php

/*
  Перед выполнением создайте таблицу:
      CREATE TABLE mycity (id NUMBER, name VARCHAR2(20));
      INSERT INTO mycity (id, name) values (1, 'Melbourne');
      CREATE TABLE mycountry (id NUMBER, name VARCHAR2(20));
      INSERT INTO mycountry (id, name) values (1, 'Australia');
      COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'SELECT mycity.name, mycountry.name
        FROM mycity, mycountry
        WHERE mycity.id = mycountry.id';
$stid = oci_parse($conn, $sql);
oci_execute($stid);
$row = oci_fetch_array($stid, OCI_ASSOC);
var_dump($row);

// Выведет только одну записаь "NAME":
//    array(1) {
//      ["NAME"]=>
//      string(9) "Australia"
//    }

// Для получения полей с повторяющимся названием используйте SQL псевдонимы (alias) для полей. Например "AS ctnm":
$sql = 'SELECT mycity.name AS ctnm, mycountry.name
        FROM mycity, mycountry
        WHERE mycity.id = mycountry.id';
$stid = oci_parse($conn, $sql);
oci_execute($stid);
$row = oci_fetch_array($stid, OCI_ASSOC);
var_dump($row);

// Выведет записи из обоих полей:
//    array(2) {
//      ["CTNM"]=>
//      string(9) "Melbourne"
//      ["NAME"]=>
//      string(9) "Australia"
//    }


oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #8 **ocifetcharray()** з полями `DATE`**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

// Устанавливаем формат даты для данного соединения.
// Для повышения производительности вместо этого
// используйте изменение формата в триггере или переменной окружения.
$stid = oci_parse($conn, "ALTER SESSION SET NLS_DATE_FORMAT = 'YYYY-MM-DD'");
oci_execute($stid);

$stid = oci_parse($conn, 'SELECT hire_date FROM employees WHERE employee_id = 188');
oci_execute($stid);
$row = oci_fetch_array($stid, OCI_ASSOC);
echo $row['HIRE_DATE'] . "<br>\n";  // выведет 1997-06-14

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #9 **ocifetcharray()** з `REF CURSOR`**

```php
<?php
/*
  Создайте PL/SQL хранимую процедуру:

  CREATE OR REPLACE PROCEDURE myproc(p1 OUT SYS_REFCURSOR) AS
  BEGIN
    OPEN p1 FOR SELECT * FROM all_objects WHERE ROWNUM < 5000;
  END;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'BEGIN myproc(:rc); END;');
$refcur = oci_new_cursor($conn);
oci_bind_by_name($stid, ':rc', $refcur, -1, OCI_B_CURSOR);
oci_execute($stid);

// Выполняет вовзращенный REF CURSOR и получает его в виде идентификатора выражения
oci_execute($refcur);
echo "<table border='1'>\n";
while (($row = oci_fetch_array($refcur, OCI_ASSOC+OCI_RETURN_NULLS)) != false) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "    <td>".($item !== null ? htmlentities($item, ENT_QUOTES) : "")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

oci_free_statement($refcur);
oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #10 Посторовий висновок за допомогою **ocifetcharray()** використовуючи `LIMIT`подібний запит**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

// Определяем версию базы данных
preg_match('/Release ([0-9]+)\./', oci_server_version($conn), $matches);
$oracleversion = $matches[1];

// Запрос, который необходимо сделать "постраничным"
$sql = 'SELECT city, postal_code FROM locations ORDER BY city';

if ($oracleversion >= 12) {
    // Используем Oracle 12c OFFSET / FETCH NEXT синтаксис
    $sql = $sql . ' OFFSET :offset ROWS FETCH NEXT :numrows ROWS ONLY';
} else {
    // Cтарые версии Oracle нуждаются в выборке с помощью подзапроса в $sql.
    // Или, если SQL выражение известно на стадии разработки, то с помощью
    // функции row_number(). Будьте осторожны и избегайте возможности
    // SQL-инъекции при объединении строк в боевом окружении.
    $sql = "SELECT * FROM (SELECT a.*, ROWNUM AS my_rnum
                           FROM ($sql) a
                           WHERE ROWNUM <= :offset + :numrows)
            WHERE my_rnum > :offset";
}

$offset  = 0;  // skip this many rows
$numrows = 5;  // return 5 rows
$stid = oci_parse($conn, $sql);
oci_bind_by_name($stid, ':numrows', $numrows);
oci_bind_by_name($stid, ':offset', $offset);
oci_execute($stid);

while (($row = oci_fetch_array($stid, OCI_ASSOC + OCI_RETURN_NULLS)) != false) {
    echo $row['CITY'] . " " . $row['POSTAL_CODE'] . "<br>\n";
}

// Выведет:
//    Beijing 190518
//    Bern 3095
//    Bombay 490231
//    Geneva 1730
//    Hiroshima 6823

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #11 **ocifetcharray()** c Oracle Database Implicit Result Sets**

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/pdborcl');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

// Требует OCI8 2.0 (или новее) и Oracle Database 12c (или новее)
// также смотрите oci_get_implicit_resultset()
$sql = 'DECLARE
           c1 SYS_REFCURSOR;
        BEGIN
           OPEN c1 FOR SELECT city, postal_code FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
           OPEN c1 FOR SELECT country_id FROM locations WHERE ROWNUM < 4 ORDER BY city;
           DBMS_SQL.RETURN_RESULT(c1);
        END;';

$stid = oci_parse($conn, $sql);
oci_execute($stid);

// Обратите внимание: oci_fetch_all и oci_fetch() нельзя неприменимы здесь
echo "<table>\n";
while (($row = oci_fetch_array($stid, OCI_ASSOC+OCI_RETURN_NULLS)) != false) {
    echo "<tr>\n";
    foreach ($row as $item) {
        echo "  <td>".($item!==null?htmlentities($item, ENT_QUOTES|ENT_SUBSTITUTE):"")."</td>\n";
    }
    echo "</tr>\n";
}
echo "</table>\n";

// Выведет:
//    Beijing 190518
//    Bern    3095
//    Bombay  490231
//    CN
//    CH
//    IN

oci_free_statement($stid);
oci_close($conn);

?>
```

### Примітки

> **Зауваження**
> 
> Індекси асоціативного масиву необхідно наводити у верхній регістр для стандартних полів Oracle, створених із реєстронезалежними назвами.

> **Зауваження**
> 
> Для запитів, що повертають велику кількість рядів, продуктивність може бути значно збільшена за допомогою збільшення значення опції [oci8.default\_prefetch](oci8.configuration.html#ini.oci8.default-prefetch) або використання [oci\_set\_prefetch()](function.oci-set-prefetch.html)

> **Зауваження**
> 
> Функція **ocifetcharray()** *трохи* повільніше [oci\_fetch\_assoc()](function.oci-fetch-assoc.html) або [oci\_fetch\_row()](function.oci-fetch-row.html), але гнучкіша.

### Дивіться також

-   [oci\_fetch()](function.oci-fetch.html) - Вибирає наступний рядок із результату в буфер
-   [oci\_fetch\_all()](function.oci-fetch-all.html) - Вибирає всі рядки з результату запиту до двомірного масиву
-   [oci\_fetch\_assoc()](function.oci-fetch-assoc.html) - Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_object()](function.oci-fetch-object.html) - Повертає наступний рядок із результату запиту у вигляді об'єкта
-   [oci\_fetch\_row()](function.oci-fetch-row.html) - Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
-   [oci\_set\_prefetch()](function.oci-set-prefetch.html) - Встановлює кількість рядків, які будуть автоматично вибрані у буфер