- [«Taint](book.taint.md)
- [Встановлення та налаштування »](taint.setup.md)

- [PHP Manual](index.md)
- [Taint](book.taint.md)
-   Вступ

# Вступ

Taint - модуль, що використовується для визначення кодів XSS (зіпсовані або
підозрілі рядки, tainted strings). Також може використовуватися для
виявлення спроб використання SQL-ін'єкцій, shell-ін'єкцій та ін.

Якщо модуль увімкнено, то коли ви передаєте підозрілий рядок (з
$\_GET, $\_POST або $\_COOKIE) деяким функціям, буде видано
попередження.

**Приклад #1 Приклад використання [Taint()](function.taint.md)**

` <?php$a = trim($_GET['a']);$file_name = '/tmp' . $a;$output    = "Welcome, {$a} !!!";$var       = "output";$sql       = "Select *  from " . $a;$sql      .= "ooxx";echo $output;print $$var;include($file_name);mysql_query($sql);?> `

Результатом виконання цього прикладу буде щось подібне:

Warning: main() [function.echo]: Attempt to echo a string that might be tainted

Warning: main() [function.echo]: Attempt to print a string that might be tainted

Warning: include() [function.include]: File path contains data that might be tainted

Warning: mysql_query() [function.mysql-query]: SQL statement contains data that might be tainted
