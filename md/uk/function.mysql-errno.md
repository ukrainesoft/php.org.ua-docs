---
navigation:
  - function.mysql-drop-db.md: « mysql\_drop\_db
  - function.mysql-error.md: mysql\_error »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_errno
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_errno

(PHP 4, PHP 5)

mysql\_errno — Повертає чисельний код помилки виконання останньої операції з MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_errno()](mysqli.errno.md)
-   [PDO::errorCode()](pdo.errorcode.md)

### Опис

```methodsynopsis
mysql_errno(resource $link_identifier = NULL): int
```

Повертає код помилки останньої функції роботи з MySQL.

Помилки роботи з MySQL більше не викликають повідомлень у PHP. Натомість використовуйте функцію **mysql\_errno()**, щоб отримати код помилки. Врахуйте, що функція повертає код помилки лише останньої виконаної функції (за винятком [mysql\_error()](function.mysql-error.md)и**mysql\_errno()**). Перевірте результат роботи функції до наступного виклику.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає код помилки останньої функції роботи з MySQL, або (нуль), якщо операцію виконано успішно.

### Приклади

**Приклад #1 Приклад використання** mysql\_errno()\*\*\*\*

```php
<?php
$link = mysql_connect("localhost", "mysql_user", "mysql_password");

if (!mysql_select_db("nonexistentdb", $link)) {
    echo mysql_errno($link) . ": " . mysql_error($link). "\n";
}

mysql_select_db("kossu", $link);
if (!mysql_query("SELECT * FROM nonexistenttable", $link)) {
    echo mysql_errno($link) . ": " . mysql_error($link) . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
1049: Unknown database 'nonexistentdb'
1146: Table 'kossu.nonexistenttable' doesn't exist
```

### Дивіться також

-   [mysql\_error()](function.mysql-error.md) \- Повертає текст помилки останньої операції з MySQL
-   [» Коди помилок MySQL](http://dev.mysql.com/doc/mysql/en/error-handling.md)
