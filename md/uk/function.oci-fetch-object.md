---
navigation:
  - function.oci-fetch-assoc.html: « ocifetchassoc
  - function.oci-fetch-row.html: ocifetchrow »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функции
title: ocifetchobject
---
# ocifetchobject

(PHP 5, PHP 7, PHP 8, PECL OCI8> = 1.1.0)

ocifetchobject — Повертає наступний рядок із результату запиту як об'єкт

### Опис

```methodsynopsis
oci_fetch_object(resource $statement, int $mode = OCI_ASSOC | OCI_RETURN_NULLS): stdClass|false
```

Повертає об'єкт, що містить наступний рядок із результату запиту. Імена властивостей об'єкта відповідають іменам стовпців у рядку. Ця функція зазвичай викликається в циклі доки не повертає **`false`** коли більше немає лав.

За подробицями щодо відображення типів даних, що здійснюється модулем OCI8, зверніться до [типів даних, що підтримуються драйвером](oci8.datatypes.md)

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [ociparse()](function.oci-parse.html) та виконаний функцією [ociexecute()](function.oci-execute.html), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає об'єкт. Кожна властивість об'єкта відповідає іменам стовпців у рядку. Якщо в результаті `запроса` більше немає рядів, то повертає **`false`**

Будь-який стовпець `LOB` повертається як дескриптор LOB.

Стовпці `DATE` повертаються у вигляді рядків, форматованих відповідно до поточних форматів дати. Стандартний формат може бути змінений за допомогою змінних оточення Oracle, таких як `NLS_LANG` або за допомогою попередньо запущеної `ALTER SESSION SET NLS_DATE_FORMAT` команди.

Вам не слід забувати про те, що Oracle повертає імена полів у верхньому регістрі, тому імена атрибутів об'єкта будуть також у верхньому регістрі. Використовуйте функцію [vardump()](function.var-dump.html) по відношенню до отриманого об'єкта для доступу до атрибутів.

Значення атрибутів відповідають **`null`** для будь-яких `NULL` полів.

### Приклади

**Приклад #1 Приклад використання **ocifetchobject()****

```php
<?php

/*
  Перед запуском создайте таблицу:
    CREATE TABLE mytab (id NUMBER, description VARCHAR2(30));
    INSERT INTO mytab (id, description) values (1, 'Fish and Chips');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, description FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_object($stid)) != false) {
    // Используйте имена атрибутов в верхнем регистре для каждого столбца Oracle
    echo $row->ID . "<br>\n";
    echo $row->DESCRIPTION . "<br>\n";
}

// Выведет:
//    1
//    Fish and Chips

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Приклад використання **ocifetchobject()** з назвами стовпців у різних регістрах**

```php
<?php

/*
Перед запуском создайте таблицу с именем столбца в различных регистрах:
    CREATE TABLE mytab (id NUMBER, "MyDescription" VARCHAR2(30));
    INSERT INTO mytab (id, "MyDescription") values (1, 'Iced Coffee');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, "MyDescription" FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_object($stid)) != false) {
    // Использование имён атрибутов в верхнем регистре для каждого столбца Oracle
    echo $row->ID . "<br>\n";
    // Использование точного написания для имени столбца с различными регистрами
    echo $row->MyDescription . "<br>\n";
}

// Выведет:
//    1
//    Iced Coffee

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 Приклад використання **ocifetchobject()** з LOB**

```php
<?php

/*
  Перед запуском создайте таблицу
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

while (($row = oci_fetch_object($stid)) != false) {
    echo $row->ID . "<br>\n";
    // Таким образом будет выведено первые 11 байт из DESCRIPTION
    echo $row->DESCRIPTION->read(11) . "<br>\n";
}

// Выведет:
//    1
//    A very long

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   [ocifetch()](function.oci-fetch.html) - Вибирає наступний рядок із результату в буфер
-   [ocifetchall()](function.oci-fetch-all.html) - Вибирає всі рядки з результату запиту до двомірного масиву
-   [ocifetchassoc()](function.oci-fetch-assoc.html) - Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [ocifetcharray()](function.oci-fetch-array.html) - Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [ocifetchrow()](function.oci-fetch-row.html) - Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
