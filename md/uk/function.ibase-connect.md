---
navigation:
  - function.ibase-commit.md: « ibase\_commit
  - function.ibase-db-info.md: ibase\_db\_info »
  - index.md: PHP Manual
  - ref.ibase.md: Функції Firebird/InterBase
title: ibase\_connect
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ibase\_connect

(PHP 5, PHP 7 < 7.4.0)

ibase\_connect — Відкриває з'єднання з базою даних

### Опис

```methodsynopsis
ibase_connect(    string $database = ?,    string $username = ?,    string $password = ?,    string $charset = ?,    int $buffers = ?,    int $dialect = ?,    string $role = ?,    int $sync = ?): resource
```

Встановлює з'єднання із сервером Firebird/InterBase.

У разі повторного виклику **ibase\_connect()** з тими ж аргументами нове посилання не буде встановлене, натомість буде повернуто ідентифікатор вже відкритого посилання. Посилання на сервер буде закрито, як тільки завершиться виконання скрипту, якщо тільки воно не було закрито раніше явним викликом [ibase\_close()](function.ibase-close.md)

### Список параметрів

`database`

Аргумент`database` повинен бути коректним шляхом до файлу бази даних на сервері, де він знаходиться. Якщо сервер не є локальним, перед ним має стояти префікс 'hostname:' (TCP / IP), 'hostname/port:' (TCP/IP з сервером interbase на порту TCP, що настроюється), '//hostname/' (NetBEUI), залежно від протоколу з'єднання.

`username`

Ім'я користувача. Може бути встановлений за допомогою директиви `ibase.default_user`php.ini.

`password`

Пароль для`username`. Може бути встановлений за допомогою директиви `ibase.default_password`php.ini.

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

Повертає ідентифікатор посилання Firebird/InterBase у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо ви отримаєте якусь помилку, наприклад "arithmetic exception, numeric overflow, or string truncation." [ibase\_query()](function.ibase-query.md) ви повинні встановити набір символів (наприклад, ISO8859\_1 або поточний набір символів).

### Приклади

**Приклад #1 Приклад використання** ibase\_connect()\*\*\*\*

```php
<?php
$host = 'localhost:/path/to/your.gdb';

$dbh = ibase_connect($host, $username, $password);
$stmt = 'SELECT * FROM tblname';
$sth = ibase_query($dbh, $stmt);
while ($row = ibase_fetch_object($sth)) {
    echo $row->email, "\n";
}
ibase_free_result($sth);
ibase_close($dbh);
?>
```

### Дивіться також

-   [ibase\_pconnect()](function.ibase-pconnect.md) \- Відкриває постійне з'єднання з базою даних InterBase
-   [ibase\_close()](function.ibase-close.md) \- Закриває з'єднання з базою даних InterBase
