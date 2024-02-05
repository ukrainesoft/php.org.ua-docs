---
navigation:
  - function.mysql-errno.md: « mysql\_errno
  - function.mysql-escape-string.md: mysql\_escape\_string »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_error
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_error

(PHP 4, PHP 5)

mysql\_error — Повертає текст помилки останньої операції з MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_error()](mysqli.error.md)
-   [PDO::errorInfo()](pdo.errorinfo.md)

### Опис

```methodsynopsis
mysql_error(resource $link_identifier = NULL): string
```

Повертає текст помилки виконання останньої функції MySQL. Помилки роботи з MySQL більше не викликають повідомлень у PHP. Натомість використовуйте функцію **mysql\_error()**, щоб отримати повідомлення про помилку. Врахуйте, що функція повертає текст помилки лише останньої виконаної функції MySQL (за винятком \*\*mysql\_error()\*\*и[mysql\_errno()](function.mysql-errno.md)), тому переконайтеся, що ви викликаєте цю функцію до виклику наступної функції MySQL.

### Список параметрів

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Повертає текст помилки виконання останньої функції MySQL, або `''` (порожній рядок), якщо операцію виконано успішно.

### Приклади

**Пример #1 Пример использования**mysql\_error()\*\*\*\*

```php
<?php
$link = mysql_connect("localhost", "mysql_user", "mysql_password");

mysql_select_db("nonexistentdb", $link);
echo mysql_errno($link) . ": " . mysql_error($link). "\n";

mysql_select_db("kossu", $link);
mysql_query("SELECT * FROM nonexistenttable", $link);
echo mysql_errno($link) . ": " . mysql_error($link) . "\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
1049: Unknown database 'nonexistentdb'
1146: Table 'kossu.nonexistenttable' doesn't exist
```

### Дивіться також

-   [mysql\_errno()](function.mysql-errno.md) \- Повертає чисельний код помилки виконання останньої операції з MySQL
-   [» Коди помилок MySQL](http://dev.mysql.com/doc/mysql/en/error-handling.md)
