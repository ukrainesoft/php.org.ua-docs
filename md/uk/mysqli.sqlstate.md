---
navigation:
  - mysqli.set-charset.md: '« mysqli::set\_charset'
  - mysqli.ssl-set.md: 'mysqli::ssl\_set »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$sqlstate'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$sqlstate

# mysqli\_sqlstate

(PHP 5, PHP 7, PHP 8)

mysqli::$sqlstate -- mysqli\_sqlstate — Повертає код стану SQLSTATE останньої операції MySQL

### Опис

Об'єктно-орієнтований стиль

string[$mysqli->sqlstate](mysqli.sqlstate.md)

Процедурний стиль

```methodsynopsis
mysqli_sqlstate(mysqli $mysql): string
```

Повертає рядок із SQLSTATE кодом останньої помилки. Цей код складається з п'яти символів . `'00000'` означає відсутність помилок. Ці коди визначені у стандарті ANSI, а також у ODBC. Переглянути список можливих значень можна на сторінці [» http://dev.mysql.com/doc/mysql/en/error-handling.md](http://dev.mysql.com/doc/mysql/en/error-handling.md)

> **Зауваження** :
> 
> Слід зазначити, що ще не всі помилки MySQL мають відображення в SQLSTATE кодах. Для подібних помилок використовується код `HY000` (Загальна помилка).

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Повертає рядок із SQLSTATE кодом останньої помилки. Цей код складається з п'яти символів . `'00000'` означає відсутність помилок.

### Приклади

**Приклад #1 Приклад використання $mysqli->sqlstate**

Об'єктно-орієнтований стиль

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* Таблица City уже существует, поэтому мы должны получить ошибку */
try {
    $mysqli->query("CREATE TABLE City (ID INT, Name VARCHAR(30))");
} catch (mysqli_sql_exception) {
    printf("Ошибка - SQLSTATE %s.\n", $mysqli->sqlstate);
}
?>
```

Процедурний стиль

```php
<?php
mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* Таблица City уже существует, поэтому мы должны получить ошибку */
try {
    mysqli_query($link, "CREATE TABLE City (ID INT, Name VARCHAR(30))");
} catch (mysqli_sql_exception) {
    printf("Ошибка - SQLSTATE %s.\n", mysqli_sqlstate($link));
}
?>
```

Результат виконання наведених прикладів:

```
Ошибка - SQLSTATE 42S01.
```

### Дивіться також

-   [mysqli\_errno()](mysqli.errno.md) \- Повертає код помилки останнього виклику функції
-   [mysqli\_error()](mysqli.error.md) \- Повертає рядок із описом останньої помилки
