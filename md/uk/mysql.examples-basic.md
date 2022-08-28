Оглядовий приклад модуля MySQL

-   [« Примеры](mysql.examples.html)
    
-   [MySQL »](ref.mysql.html)
    
-   [PHP Manual](index.html)
    
-   [Примеры](mysql.examples.html)
    
-   Оглядовий приклад модуля MySQL
    

## Оглядовий приклад модуля MySQL

Цей простий приклад показує, як з'єднатися з базою даних, виконати запит, надрукувати результат та від'єднатися.

**Приклад #1 Приклад роботи з MySQL**

```php
<?php
// Соединяемся, выбираем базу данных
$link = mysql_connect('mysql_host', 'mysql_user', 'mysql_password')
    or die('Не удалось соединиться: ' . mysql_error());
echo 'Соединение успешно установлено';
mysql_select_db('my_database') or die('Не удалось выбрать базу данных');

// Выполняем SQL-запрос
$query = 'SELECT * FROM my_table';
$result = mysql_query($query) or die('Запрос не удался: ' . mysql_error());

// Выводим результаты в html
echo "<table>\n";
while ($line = mysql_fetch_array($result, MYSQL_ASSOC)) {
    echo "\t<tr>\n";
    foreach ($line as $col_value) {
        echo "\t\t<td>$col_value</td>\n";
    }
    echo "\t</tr>\n";
}
echo "</table>\n";

// Освобождаем память от результата
mysql_free_result($result);

// Закрываем соединение
mysql_close($link);
?>
```