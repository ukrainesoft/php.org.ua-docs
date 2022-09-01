---
navigation:
  - function.mysql-error.html: « mysqlerror
  - function.mysql-fetch-array.html: mysqlfetcharray »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysqlescapestring
---
# mysqlescapestring

(PHP 4> = 4.0.3, PHP 5)

mysqlescapestring — Екранує рядок для використання у mysqlquery

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.md)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.md) або [PDOMySQL](ref.pdo-mysql.md). Також дивіться розділ [MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqliescapestring()](function.mysqli-escape-string.md)
-   [PDO::quote()](pdo.quote.md)

### Опис

```methodsynopsis
mysql_escape_string(string $unescaped_string): string
```

Функція екранує `unescaped_string` таким чином, після чого її можна безпечно використовувати в [mysqlquery()](function.mysql-query.md). Ця функція застаріла.

Функція ідентична [mysqlrealescapestring()](function.mysql-real-escape-string.html), виключаючи той факт, що [mysqlrealescapestring()](function.mysql-real-escape-string.md) приймає параметром ще й ідентифікатор з'єднання та екранує рядок з урахуванням поточного кодування . **mysqlescapestring()** не робить цього і результат роботи не залежить від кодування, в якому ви працюєте з БД.

### Список параметрів

`unescaped_string`

Рядок, що екранується.

### Значення, що повертаються

Повертає рядок, що екранується.

### Приклади

**Приклад #1 Приклад використання **mysqlescapestring()****

```php
<?php
$item = "Zak's Laptop";
$escaped_item = mysql_escape_string($item);
printf("Escaped string: %s\n", $escaped_item);
?>
```

Результат виконання цього прикладу:

```
Escaped string: Zak\'s Laptop
```

### Примітки

> **Зауваження**
> 
> **mysqlescapestring()** не екранує символи `%` і `_`

### Дивіться також

-   [mysqlrealescapestring()](function.mysql-real-escape-string.md) - Екранує спеціальні символи у рядках для використання у виразах SQL
-   [addslashes()](function.addslashes.md) - Екранує рядок за допомогою слішів
-   Директиву [magicquotesgpc](info.configuration.html#ini.magic-quotes-gpc)
