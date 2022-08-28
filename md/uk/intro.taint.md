Вступ

-   [« Taint](book.taint.html)
    
-   [Установка и настройка »](taint.setup.html)
    
-   [PHP Manual](index.html)
    
-   [Taint](book.taint.html)
    
-   Вступ
    

# Вступ

Taint - модуль, використовуваний визначення кодів XSS (зіпсовані чи підозрілі рядки, tainted strings). Також може використовуватися виявлення спроб використання SQL-ін'єкцій, shell-ін'єкцій тощо.

Якщо модуль увімкнено, то коли ви передаєте підозрілий рядок (з $GET, $POST або $COOKIE) деяким функціям буде видано попередження.

**Приклад #1 Приклад використання [Taint()](function.taint.html)**

```php
<?php
$a = trim($_GET['a']);

$file_name = '/tmp' .  $a;
$output    = "Welcome, {$a} !!!";
$var       = "output";
$sql       = "Select *  from " . $a;
$sql      .= "ooxx";

echo $output;

print $$var;

include($file_name);

mysql_query($sql);
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Warning: main() [function.echo]: Attempt to echo a string that might be tainted

Warning: main() [function.echo]: Attempt to print a string that might be tainted

Warning: include() [function.include]: File path contains data that might be tainted

Warning: mysql_query() [function.mysql-query]: SQL statement contains data that might be tainted
```