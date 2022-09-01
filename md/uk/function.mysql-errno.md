---
navigation:
  - function.mysql-drop-db.html: « mysqldropдб
  - function.mysql-error.html: mysqlerror »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlerrno
---
# mysqlerrno

(PHP 4, PHP 5)

mysqlerrno — Повертає чисельний код помилки виконання останньої операції з MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і вилучений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Дивіться також інструкцію [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqlierrno()](mysqli.errno.md)
-   [PDO::errorCode()](pdo.errorcode.md)

### Опис

```methodsynopsis
mysql_errno(resource $link_identifier = NULL): int
```

Повертає код помилки останньої функції роботи з MySQL.

Помилки роботи з MySQL більше не викликають повідомлень у PHP. Натомість використовуйте функцію **mysqlerrno()**, щоб отримати код помилки. Врахуйте, що функція повертає код помилки лише останньої виконаної функції (за винятком [mysqlerror()](function.mysql-error.md) і **mysqlerrno()**). Перевірте результат роботи функції до наступного виклику.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, використовується останнє з'єднання, відкрите [mysqlconnect()](function.mysql-connect.html). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysqlconnect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає код помилки останньої функції роботи з MySQL, або `0` (нуль), якщо операцію виконано успішно.

### Приклади

**Приклад #1 Приклад використання **mysqlerrno()****

```php
<?php
$link = mysql_connect("localhost", "mysql_user", "mysql_password");

if (!mysql_select_db("nonexistentdb", $link)) {
    echo mysql_errno($link) . ": " . mysql_error($link). "\n";
}

mysql_select_db("kossu", $link);
if (!mysql_query("SELECT * FROM nonexistenttable", $link)) {
    echo mysql_errno($link) . ": " . mysql_error($link) . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
1049: Unknown database 'nonexistentdb'
1146: Table 'kossu.nonexistenttable' doesn't exist
```

### Дивіться також

-   [mysqlerror()](function.mysql-error.md) - Повертає текст помилки останньої операції з MySQL
-   [» Коди помилок MySQL](http://dev.mysql.com/doc/mysql/en/error-handling.md)
