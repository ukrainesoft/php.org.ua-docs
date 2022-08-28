Готує результуючий набір на сервері для використання

-   [« mysqli::thread\_safe](mysqli.thread-safe.html)
    
-   [mysqli::$warning\_count »](mysqli.warning-count.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Готує результуючий набір на сервері для використання
    

# mysqli::useresult

# mysqliuseresult

(PHP 5, PHP 7, PHP 8)

mysqli::useresult -- mysqliuseresult — Готує результуючий набір на сервері для використання

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::use_result(): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_use_result(mysqli $mysql): mysqli_result|false
```

Використовується для підготовки результуючого набору останнього запиту, запущеного функцією [mysqli\_real\_query()](mysqli.real-query.html)

Щоб результати запиту стали доступними, після запиту необхідно викликати або цю функцію, або [mysqli\_store\_result()](mysqli.store-result.html). Також виклик будь-якому з них запобігатиме відмову наступних запитів на цьому ж з'єднанні.

> **Зауваження**
> 
> **mysqliuseresult()** не передає весь результуючий набір на клієнта, а отже неможливо скористатися функцією [mysqli\_data\_seek()](mysqli-result.data-seek.html)для переміщення по ньому. Для цього потрібно скористатися функцією [mysqli\_store\_result()](mysqli.store-result.html). . **mysqliuseresult()** не слід використовувати, якщо на стороні клієнта дані результуючого набору довго обробляються, оскільки це затримує роботу сервера і не дає іншим процесам оновлювати таблиці, дані з яких є в результуючому наборі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає небуферизований об'єкт результату запиту або **`false`** у разі помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::useresult()****

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query  = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполняем мультизапрос */
if ($mysqli->multi_query($query)) {
    do {
        /* получаем первый результирующий набор */
        if ($result = $mysqli->use_result()) {
            while ($row = $result->fetch_row()) {
                printf("%s\n", $row[0]);
            }
            $result->close();
        }
        /* печатаем разделитель */
        if ($mysqli->more_results()) {
            printf("-----------------\n");
        }
    } while ($mysqli->next_result());
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query  = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполняем мультизапрос */
if (mysqli_multi_query($link, $query)) {
    do {
        /* получаем первый результирующий набор */
        if ($result = mysqli_use_result($link)) {
            while ($row = mysqli_fetch_row($result)) {
                printf("%s\n", $row[0]);
            }
            mysqli_free_result($result);
        }
        /* печатаем разделитель */
        if (mysqli_more_results($link)) {
            printf("-----------------\n");
        }
    } while (mysqli_next_result($link));
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання даних прикладів:

```
my_user@localhost
-----------------
Amersfoort
Maastricht
Dordrecht
Leiden
Haarlemmermeer
```

### Дивіться також

-   [mysqli\_real\_query()](mysqli.real-query.html) - Виконання SQL запиту
-   [mysqli\_store\_result()](mysqli.store-result.html) - передає на клієнта результуючий набір останнього запиту