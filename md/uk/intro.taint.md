---
navigation:
  - book.taint.md: « Taint
  - taint.setup.md: Встановлення та налаштування "
  - index.md: PHP Manual
  - book.taint.md: Taint
title: Вступ
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Вступ

Taint — модуль визначення кодів XSS (зіпсовані або підозрілі рядки, tainted strings). Також може бути корисним для виявлення спроб впровадження SQL-ін'єкцій, shell-ін'єкцій і т.д.

Якщо модуль увімкнено, то коли ви передаєте підозрілий рядок (з $\_GET, $\_POST або $\_COOKIE) деяким функціям буде видано попередження.

**Приклад #1 Приклад использования[Taint()](function.taint.md)**

```php
<?php
$a = trim($_GET['a']);

$file_name = '/tmp' .  $a;
$output    = "Welcome, {$a} !!!";
$var       = "output";
$sql       = "Select *  from " . $a;
$sql      .= "ooxx";

echo $output;

print $$var;

include $file_name;

mysql_query($sql);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Warning: main() [function.echo]: Attempt to echo a string that might be tainted

Warning: main() [function.echo]: Attempt to print a string that might be tainted

Warning: include() [function.include]: File path contains data that might be tainted

Warning: mysql_query() [function.mysql-query]: SQL statement contains data that might be tainted
```
