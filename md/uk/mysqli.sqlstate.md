---
navigation:
  - mysqli.set-charset.md: '« mysqli::setcharset'
  - mysqli.ssl-set.md: 'mysqli::sslset »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$sqlstate'
---
# mysqli::$sqlstate

# mysqlisqlstate

(PHP 5, PHP 7, PHP 8)

mysqli::$sqlstate -- mysqlisqlstate — Повертає код стану SQLSTATE останньої операції MySQL

### Опис

Об'єктно-орієнтований стиль

string [$mysqli->sqlstate](mysqli.sqlstate.md)

Процедурний стиль

```methodsynopsis
mysqli_sqlstate(mysqli $mysql): string
```

Повертає рядок із SQLSTATE кодом останньої помилки. Цей код складається з п'яти символів . `'00000'` означає відсутність помилок. Ці коди визначені у стандарті ANSI, а також у ODBC. Переглянути список можливих значень можна на сторінці [» http://dev.mysql.com/doc/mysql/en/error-handling.html](http://dev.mysql.com/doc/mysql/en/error-handling.md)

> **Зауваження**
> 
> Слід зазначити, що ще не всі помилки MySQL мають відображення в SQLSTATE кодах. Для подібних помилок використовується код `HY000` (Загальна помилка).

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

### Значення, що повертаються

Повертає рядок із SQLSTATE кодом останньої помилки. Цей код складається з п'яти символів . `'00000'` означає відсутність помилок.

### Приклади

**Приклад #1 Приклад використання $mysqli->sqlstate**

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* таблица City уже существует, так что мы должны получить ошибку */
if (!$mysqli->query("CREATE TABLE City (ID INT, Name VARCHAR(30))")) {
    printf("Ошибка - SQLSTATE %s.\n", $mysqli->sqlstate);
}

$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

/* таблица City уже существует, так что мы должны получить ошибку */
if (!mysqli_query($link, "CREATE TABLE City (ID INT, Name VARCHAR(30))")) {
    printf("Ошибка - SQLSTATE %s.\n", mysqli_sqlstate($link));
}

mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
Ошибка - SQLSTATE 42S01.
```

### Дивіться також

-   [mysqlierrno()](mysqli.errno.md) - Повертає код помилки останнього виклику функції
-   [mysqlierror()](mysqli.error.md) - Повертає рядок із описом останньої помилки
