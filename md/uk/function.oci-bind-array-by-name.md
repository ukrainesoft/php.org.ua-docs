Пов'язує PHP масив з масивом Oracle PL/SQL

-   [« OCI8 Функции](ref.oci8.html)
    
-   [ocibindбname »](function.oci-bind-by-name.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Пов'язує PHP масив з масивом Oracle PL/SQL
    

# ocibindarrayбname

(PHP 5> = 5.1.2, PHP 7, PHP 8, PECL OCI8> = 1.2.0)

ocibindarrayбname - Зв'язує PHP масив з масивом Oracle PL/SQL

### Опис

```methodsynopsis
oci_bind_array_by_name(    resource $statement,    string $param,    array &$var,    int $max_array_length,    int $max_item_length = -1,    int $type = SQLT_AFC): bool
```

Пов'язує PHP масив `var` з вказівником Oracle `param` на масив Oracle PL/SQL. Напрямок, введення або висновок, для якого використовуватиметься масив, буде визначатися під час виконання.

### Список параметрів

`statement`

Ідентифікатор допустимого виразу OCI.

`param`

Вказівник на масив Oracle.

`var`

Масив.

`max_array_length`

Задає максимальний розмір для вихідного та результуючого масивів.

`max_item_length`

Визначає максимальний розмір значень масиву. Якщо не встановлено або дорівнює -1, **ocibindarrayбname()** знайде найбільший елемент у вихідному масиві і використовує його розмір як цю настройку.

`type`

Використовується для завдання типу значень PL/SQL масиву. Дивіться список нижче:

-   **`SQLT_NUM`** - для масивів із елементами типу NUMBER.
    
-   **`SQLT_INT`** - для масивів з елементами типу INTEGER (Примітка: INTEGER - синонім типу NUMBER(38), проте тип **`SQLT_NUM`** у цьому випадку не працюватиме, навіть незважаючи на те, що вони синонімічні).
    
-   **`SQLT_FLT`** - для масивів із елементами типу FLOAT.
    
-   **`SQLT_AFC`** - для масивів із елементами типу CHAR.
    
-   **`SQLT_CHR`** - для масивів із елементами типу VARCHAR2.
    
-   **`SQLT_VCS`** - для масивів із елементами типу VARCHAR.
    
-   **`SQLT_AVC`** - для масивів із елементами типу CHARZ.
    
-   **`SQLT_STR`** - для масивів із елементами типу STRING.
    
-   **`SQLT_LVC`** - для масивів із елементами типу LONG VARCHAR.
    
-   **`SQLT_ODT`** - для масивів із елементами типу DATE.
    

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ocibindarrayбname()****

```php
<?php

$conn = oci_connect("hr", "hrpwd", "localhost/XE");
if (!$conn) {
    $m = oci_error();
    trigger_error(htmlentities($m['message']), E_USER_ERROR);
}

$create = "CREATE TABLE bind_example(name VARCHAR(20))";
$stid = oci_parse($conn, $create);
oci_execute($stid);

$create_pkg = "
CREATE OR REPLACE PACKAGE ARRAYBINDPKG1 AS
  TYPE ARRTYPE IS TABLE OF VARCHAR(20) INDEX BY BINARY_INTEGER;
  PROCEDURE iobind(c1 IN OUT ARRTYPE);
END ARRAYBINDPKG1;";
$stid = oci_parse($conn, $create_pkg);
oci_execute($stid);

$create_pkg_body = "
CREATE OR REPLACE PACKAGE BODY ARRAYBINDPKG1 AS
  CURSOR CUR IS SELECT name FROM bind_example;
  PROCEDURE iobind(c1 IN OUT ARRTYPE) IS
    BEGIN
    -- Bulk Insert
    FORALL i IN INDICES OF c1
      INSERT INTO bind_example VALUES (c1(i));

    -- Fetch and reverse
    IF NOT CUR%ISOPEN THEN
      OPEN CUR;
    END IF;
    FOR i IN REVERSE 1..5 LOOP
      FETCH CUR INTO c1(i);
      IF CUR%NOTFOUND THEN
        CLOSE CUR;
        EXIT;
      END IF;
    END LOOP;
  END iobind;
END ARRAYBINDPKG1;";
$stid = oci_parse($conn, $create_pkg_body);
oci_execute($stid);

$stid = oci_parse($conn, "BEGIN arraybindpkg1.iobind(:c1); END;");
$array = array("one", "two", "three", "four", "five");
oci_bind_array_by_name($stid, ":c1", $array, 5, -1, SQLT_CHR);
oci_execute($stid);

var_dump($array);

?>
```