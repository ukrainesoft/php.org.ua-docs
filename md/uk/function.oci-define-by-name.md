Порівняє змінну PHP стовпцю результату запиту

-   [« ociconnect](function.oci-connect.html)
    
-   [ocierror »](function.oci-error.html)
    
-   [PHP Manual](index.html)
    
-   [OCI8 Функции](ref.oci8.html)
    
-   Порівняє змінну PHP стовпцю результату запиту
    

# ocidefineбname

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocidefineбname — Порівняє змінну PHP стовпцю результату запиту

### Опис

```methodsynopsis
oci_define_by_name(    resource $statement,    string $column,    mixed &$var,    int $type = 0): bool
```

Зіставляє змінну PHP стовпцю результату запиту, отриманого за допомогою [ocifetch()](function.oci-fetch.html)

Виклик **ocidefineбname()** повинен проводитися до запуску [ociexecute()](function.oci-execute.html)

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [ociparse()](function.oci-parse.html) та виконаний функцією [ociexecute()](function.oci-execute.html), або ідентифікатор виразу `REF CURSOR`

`column`

Ім'я стовпця використаного у запиті.

Використовуйте верхній регістр для стандартних незалежних імен стовпців Oracle. Використовуйте точне написання імені стовпця для реєстрозалежних імен.

`var`

Змінна PHP, призначена для зберігання поверненого значення.

`type`

Тип даних, що повертаються. Зазвичай не потрібно. Майте на увазі, що перетворення Oracle-даних не виконуються. Наприклад, `SQLT_INT` буде проігноровано і повернені дані будуть як і раніше у вигляді `SQLT_CHR`

Якщо вам потрібно призначити змінну абстрактного типу даних (LOB/ROWID/BFILE), її необхідно спочатку створити за допомогою [ocinewdescriptor()](function.oci-new-descriptor.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ocidefineбname()****

```php
<?php

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$sql = 'SELECT location_id, city FROM locations WHERE location_id < 1200';
$stid = oci_parse($conn, $sql);

// Переменные ДОЛЖНЫ быть определены перед запуском
oci_define_by_name($stid, 'LOCATION_ID', $locid);
oci_define_by_name($stid, 'CITY', $city);

oci_execute($stid);

//  Каждый результат запроса помещает в заранее определённую переменную следующую строку данных
while (oci_fetch($stid)) {
    echo "ID местоположения $locid - $city<br>\n";
}

// Выведет:
//   ID местоположения 1000 - Roma
//   ID местоположения 1100 - Venice

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Приклад використання **ocidefineбname()** з реєстрозалежними іменами стовпців**

```php
<?php

/*
  До запуска, создаётся таблица со столбцом, имеющим регистрозависимое имя
    CREATE TABLE mytab (id NUMBER, "MyDescription" VARCHAR2(30));
    INSERT INTO mytab (id, "MyDescription") values (1, 'Iced Coffee');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM mytab');

// Используется верхний регистр для регистронезависимых имён столбцов
oci_define_by_name($stid, 'ID', $id);

// Используется точное написание для регистрозависимых имён столбцов
oci_define_by_name($stid, 'MyDescription', $mydesc);

oci_execute($stid);

while (oci_fetch($stid)) {
    echo "Идентификатор $id - $mydesc<br>\n";
}

// Выведет:
//   Идентификатор 1 - Iced Coffee

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 Приклад використання **ocidefineбname()** зі стовпцями типу LOB**

```php
<?php

/*
  Перед запуском создаются таблицы:
    CREATE TABLE mytab (id NUMBER, fruit CLOB);
    INSERT INTO mytab (id, fruit) values (1, 'apple');
    INSERT INTO mytab (id, fruit) values (2, 'orange');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM mytab');

// Переменные ДОЛЖНЫ быть определены перед запуском
oci_define_by_name($stid, 'ID', $id);
oci_define_by_name($stid, 'FRUIT', $fruit);  // $fruit станет дескриптором LOB

oci_execute($stid);

while (oci_fetch($stid)) {
    echo $id . " - " . $fruit->load(100) . "<br>\n";
}

// Выведет:
//   1 - apple
//   2 - orange

$fruit->free();
oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #4 Приклад використання **ocidefineбname()** з наведеними типами**

```php
<?php

/*
  Перед запуском создаётся таблица:
    CREATE TABLE mytab (id NUMBER, fruit CLOB);
    INSERT INTO mytab (id, fruit) values (1, 'apple');
    INSERT INTO mytab (id, fruit) values (2, 'orange');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT * FROM mytab');

// Переменные ДОЛЖНЫ быть определены перед запуском
oci_define_by_name($stid, 'ID', $id);

$fruit = oci_new_descriptor($conn, OCI_D_LOB);
oci_define_by_name($stid, 'FRUIT', $fruit, OCI_D_CLOB);

oci_execute($stid);

while (oci_fetch($stid)) {
    echo $id . " - " . $fruit->load(100) . "<br>\n";
}

// Выведет:
//   1 - apple
//   2 - orange

$fruit->free();
oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   [ocifetch()](function.oci-fetch.html) - Вибирає наступний рядок із результату в буфер
-   [ocinewdescriptor()](function.oci-new-descriptor.html) - Ініціалізує новий дескриптор об'єкта LOB чи FILE