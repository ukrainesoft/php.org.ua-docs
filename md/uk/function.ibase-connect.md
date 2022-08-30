Відкриває з'єднання з базою даних

-   [« ibasecommit](function.ibase-commit.html)
    
-   [ibaseдбinfo »](function.ibase-db-info.html)
    
-   [PHP Manual](index.md)
    
-   [Функции Firebird/InterBase](ref.ibase.md)
    
-   Відкриває з'єднання з базою даних
    

# ibaseconnect

(PHP 5, PHP 7 < 7.4.0)

ibaseconnect — Відкриває з'єднання з базою даних

### Опис

```methodsynopsis
ibase_connect(    string $database = ?,    string $username = ?,    string $password = ?,    string $charset = ?,    int $buffers = ?,    int $dialect = ?,    string $role = ?,    int $sync = ?): resource
```

Встановлює з'єднання із сервером Firebird/InterBase.

У разі повторного виклику **ibaseconnect()** з тими ж аргументами нове посилання не буде встановлене, натомість буде повернуто ідентифікатор вже відкритого посилання. Посилання на сервер буде закрито, як тільки завершиться виконання скрипту, якщо тільки воно не було закрито раніше явним викликом [ibaseclose()](function.ibase-close.html)

### Список параметрів

`database`

Аргумент `database` повинен бути коректним шляхом до файлу бази даних на сервері, де він знаходиться. Якщо сервер не є локальним, перед ним має стояти префікс 'hostname:' (TCP / IP), 'hostname/port:' (TCP/IP з сервером interbase на порту TCP, що настроюється), '//hostname/' (NetBEUI), залежно від протоколу з'єднання.

`username`

Ім'я користувача. Може бути встановлений за допомогою директиви `ibase.default_user` php.ini.

`password`

Пароль для `username`. Може бути встановлений за допомогою директиви `ibase.default_password` php.ini.

`charset`

`charset` є набором за промовчанням для бази даних.

`buffers`

`buffers` - це кількість буферів бази даних, що виділяються для кеша за сервера. Якщо 0 або не вказано, сервер вибирає власний за промовчанням.

`dialect`

`dialect` вибирає діалект SQL за замовчуванням для будь-якого оператора, що виконується у з'єднанні, за умовчанням він відповідає максимальному підтримуваному клієнтським бібліотекам.

`role`

Функціонально лише з InterBase 5 та вище.

`sync`

### Значення, що повертаються

Повертає ідентифікатор посилання Firebird/InterBase у разі успішного виконання або **`false`** у разі виникнення помилки.

### Помилки

Якщо ви отримаєте якусь помилку, наприклад "arithmetic exception, numeric overflow, or string truncation." [ibasequery()](function.ibase-query.html) ви повинні встановити набір символів (наприклад, ISO88591 або поточний набір символів).

### Приклади

**Приклад #1 Приклад використання **ibaseconnect()****

```php
<?php
$host = 'localhost:/path/to/your.gdb';

$dbh = ibase_connect($host, $username, $password);
$stmt = 'SELECT * FROM tblname';
$sth = ibase_query($dbh, $stmt);
while ($row = ibase_fetch_object($sth)) {
    echo $row->email, "\n";
}
ibase_free_result($sth);
ibase_close($dbh);
?>
```

### Дивіться також

-   [ibasepconnect()](function.ibase-pconnect.html) - Відкриває постійне з'єднання з базою даних InterBase
-   [ibaseclose()](function.ibase-close.html) - Закриває з'єднання з базою даних InterBase