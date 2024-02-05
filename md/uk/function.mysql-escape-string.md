---
navigation:
  - function.mysql-error.md: « mysql\_error
  - function.mysql-fetch-array.md: mysql\_fetch\_array »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_escape\_string
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_escape\_string

(PHP 4 >= 4.0.3, PHP 5)

mysql\_escape\_string — Екранує рядок для використання у mysql\_query

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Так же смотрите раздел[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_escape\_string()](function.mysqli-escape-string.md)
-   [PDO::quote()](pdo.quote.md)

### Опис

```methodsynopsis
mysql_escape_string(string $unescaped_string): string
```

Функція екранує `unescaped_string` таким чином, після чого її можна безпечно використовувати в [mysql\_query()](function.mysql-query.md)Данная функция устарела.

Функція ідентична [mysql\_real\_escape\_string()](function.mysql-real-escape-string.md), виключаючи той факт, що [mysql\_real\_escape\_string()](function.mysql-real-escape-string.md) приймає параметром ще й ідентифікатор з'єднання та екранує рядок з урахуванням поточного кодування . **mysql\_escape\_string()** не робить цього і результат роботи не залежить від кодування, в якому ви працюєте з БД.

### Список параметрів

`unescaped_string`

Рядок, що екранується.

### Значення, що повертаються

Повертає рядок, що екранується.

### Приклади

**Приклад #1 Приклад використання** mysql\_escape\_string()\*\*\*\*

```php
<?php
$item = "Zak's Laptop";
$escaped_item = mysql_escape_string($item);
printf("Escaped string: %s\n", $escaped_item);
?>
```

Результат виконання наведеного прикладу:

```
Escaped string: Zak\'s Laptop
```

### Примітки

> **Зауваження** :
> 
> **mysql\_escape\_string()** не екранує символи `%`и`_`

### Дивіться також

-   [mysql\_real\_escape\_string()](function.mysql-real-escape-string.md) \- Екранує спеціальні символи у рядках для використання у виразах SQL
