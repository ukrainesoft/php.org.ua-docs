Екранує рядок для використання в mysqlquery

-   [« mysqlerror](function.mysql-error.html)
    
-   [mysqlfetcharray »](function.mysql-fetch-array.html)
    
-   [PHP Manual](index.html)
    
-   [MySQL](ref.mysql.html)
    
-   Екранує рядок для використання в mysqlquery
    

# mysqlescapestring

(PHP 4> = 4.0.3, PHP 5)

mysqlescapestring — Екранує рядок для використання у mysqlquery

**Увага**

Ця функція оголошена застарілою в PHP 4.3.0, і, разом з [модулем MySQL](book.mysql.html)видалено PHP в 7.0.0. Замість неї використовуйте модулі, що активно розвиваються. [MySQLi](book.mysqli.html) або [PDOMySQL](ref.pdo-mysql.html). Також дивіться розділ [MySQL: выбор API](mysqlinfo.api.choosing.html). Альтернативи для цієї функції:

-   [mysqliescapestring()](function.mysqli-escape-string.html)
-   [PDO::quote()](pdo.quote.html)

### Опис

```methodsynopsis
mysql_escape_string(string $unescaped_string): string
```

Функція екранує `unescaped_string` таким чином, після чого її можна безпечно використовувати в [mysqlquery()](function.mysql-query.html). Ця функція застаріла.

Функція ідентична [mysqlrealescapestring()](function.mysql-real-escape-string.html), виключаючи той факт, що [mysqlrealescapestring()](function.mysql-real-escape-string.html) приймає параметром ще й ідентифікатор з'єднання та екранує рядок з урахуванням поточного кодування . **mysqlescapestring()** не робить цього і результат роботи не залежить від кодування, в якому ви працюєте з БД.

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

-   [mysqlrealescapestring()](function.mysql-real-escape-string.html) - Екранує спеціальні символи у рядках для використання у виразах SQL
-   [addslashes()](function.addslashes.html) - Екранує рядок за допомогою слішів
-   Директиву [magicquotesgpc](info.configuration.html#ini.magic-quotes-gpc)