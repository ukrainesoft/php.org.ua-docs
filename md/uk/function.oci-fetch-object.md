---
navigation:
  - function.oci-fetch-assoc.md: « oci\_fetch\_assoc
  - function.oci-fetch-row.md: oci\_fetch\_row »
  - index.md: PHP Manual
  - ref.oci8.md: OCI8 Функції
title: oci\_fetch\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# oci\_fetch\_object

(PHP 5, PHP 7, PHP 8, PECL OCI8 >= 1.1.0)

oci\_fetch\_object — Повертає наступний рядок із результату запиту як об'єкт

### Опис

```methodsynopsis
oci_fetch_object(resource $statement, int $mode = OCI_ASSOC | OCI_RETURN_NULLS): stdClass|false
```

Повертає об'єкт, що містить наступний рядок із результату запиту. Імена властивостей об'єкта відповідають іменам стовпців у рядку. Ця функція зазвичай викликається в циклі доки не повертає **`false`** коли більше немає лав.

Для отримання детальнішої інформації щодо відображення типів даних модуля OCI8 зверніться до [типів даних, що підтримуються драйвером](oci8.datatypes.md)

### Список параметрів

`statement`

Коректний ідентифікатор виразу OCI8, отриманий з [oci\_parse()](function.oci-parse.md) та виконаний функцією [oci\_execute()](function.oci-execute.md), або ідентифікатор виразу `REF CURSOR`

### Значення, що повертаються

Повертає об'єкт. Кожна властивість об'єкта відповідає іменам стовпців у рядку. Якщо в результаті `запиту` більше немає рядів, то повертає **`false`**

Будь-який стовпець `LOB` повертається як дескриптор LOB.

Стовпці `DATE` повертаються у вигляді рядків, форматованих відповідно до поточних форматів дати. Стандартний формат може бути змінений за допомогою змінних оточення Oracle, таких як `NLS_LANG` або за допомогою попередньо запущеної `ALTER SESSION SET NLS_DATE_FORMAT` команди.

Вам не слід забувати про те, що Oracle повертає імена полів у верхньому регістрі, тому імена атрибутів об'єкта будуть також у верхньому регістрі. Використовуйте функцію [var\_dump()](function.var-dump.md) по відношенню до отриманого об'єкта для доступу до атрибутів.

Значення атрибутів відповідають **`null`** для будь-яких `NULL` полів.

### Приклади

**Приклад #1 Приклад використання** oci\_fetch\_object()\*\*\*\*

```php
<?php

/*
  Перед запуском создайте таблицу:
    CREATE TABLE mytab (id NUMBER, description VARCHAR2(30));
    INSERT INTO mytab (id, description) values (1, 'Fish and Chips');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, description FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_object($stid)) != false) {
    // Используйте имена атрибутов в верхнем регистре для каждого столбца Oracle
    echo $row->ID . "<br>\n";
    echo $row->DESCRIPTION . "<br>\n";
}

// Выведет:
//    1
//    Fish and Chips

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #2 Приклад використання** oci\_fetch\_object()\*\* з назвами стовпців у різних регістрах\*\*

```php
<?php

/*
Перед запуском создайте таблицу с именем столбца в различных регистрах:
    CREATE TABLE mytab (id NUMBER, "MyDescription" VARCHAR2(30));
    INSERT INTO mytab (id, "MyDescription") values (1, 'Iced Coffee');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, "MyDescription" FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_object($stid)) != false) {
    // Использование имён атрибутов в верхнем регистре для каждого столбца Oracle
    echo $row->ID . "<br>\n";
    // Использование точного написания для имени столбца с различными регистрами
    echo $row->MyDescription . "<br>\n";
}

// Выведет:
//    1
//    Iced Coffee

oci_free_statement($stid);
oci_close($conn);

?>
```

**Приклад #3 Приклад використання** oci\_fetch\_object()**с LOB**

```php
<?php

/*
  Перед запуском создайте таблицу
    CREATE TABLE mytab (id NUMBER, description CLOB);
    INSERT INTO mytab (id, description) values (1, 'A very long string');
    COMMIT;
*/

$conn = oci_connect('hr', 'welcome', 'localhost/XE');
if (!$conn) {
    $e = oci_error();
    trigger_error(htmlentities($e['message'], ENT_QUOTES), E_USER_ERROR);
}

$stid = oci_parse($conn, 'SELECT id, description FROM mytab');
oci_execute($stid);

while (($row = oci_fetch_object($stid)) != false) {
    echo $row->ID . "<br>\n";
    // Таким образом будет выведено первые 11 байт из DESCRIPTION
    echo $row->DESCRIPTION->read(11) . "<br>\n";
}

// Выведет:
//    1
//    A very long

oci_free_statement($stid);
oci_close($conn);

?>
```

### Дивіться також

-   [oci\_fetch()](function.oci-fetch.md) \- Вибирає наступний рядок із результату в буфер
-   [oci\_fetch\_all()](function.oci-fetch-all.md) \- Вибирає всі рядки з результату запиту до двомірного масиву
-   [oci\_fetch\_assoc()](function.oci-fetch-assoc.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного масиву
-   [oci\_fetch\_array()](function.oci-fetch-array.md) \- Повертає наступний рядок із результату запиту у вигляді асоціативного чи нумерованого масиву
-   [oci\_fetch\_row()](function.oci-fetch-row.md) \- Повертає наступний рядок із результату запиту у вигляді нумерованого масиву
