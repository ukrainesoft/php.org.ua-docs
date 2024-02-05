---
navigation:
  - pgsql.examples.md: « Приклади
  - pgsql.examples-queries.md: Базове використання »
  - index.md: PHP Manual
  - pgsql.examples.md: Приклади
title: Базове використання
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Базове використання

Цей простий приклад показує, як виконати з'єднання з БД, надіслати запит, вивести його результат і закрити з'єднання з PostgreSQL.

**Приклад #1 Приклад роботи з модулем PostgreSQL**

```php
<?php
// Соединение, выбор базы данных
$dbconn = pg_connect("host=localhost dbname=publishing user=www password=foo")
    or die('Не удалось соединиться: ' . pg_last_error());

// Выполнение SQL-запроса
$query = 'SELECT * FROM authors';
$result = pg_query($query) or die('Ошибка запроса: ' . pg_last_error());

// Вывод результатов в HTML
echo "<table>\n";
while ($line = pg_fetch_array($result, null, PGSQL_ASSOC)) {
    echo "\t<tr>\n";
    foreach ($line as $col_value) {
        echo "\t\t<td>$col_value</td>\n";
    }
    echo "\t</tr>\n";
}
echo "</table>\n";

// Очистка результата
pg_free_result($result);

// Закрытие соединения
pg_close($dbconn);
?>
```
