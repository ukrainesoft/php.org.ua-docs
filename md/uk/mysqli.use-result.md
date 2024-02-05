---
navigation:
  - mysqli.thread-safe.md: '« mysqli::thread\_safe'
  - mysqli.warning-count.md: 'mysqli::$warning\_count »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::use\_result'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::use\_result

# mysqli\_use\_result

(PHP 5, PHP 7, PHP 8)

mysqli::use\_result -- mysqli\_use\_result — Готує результуючий набір на сервері для використання

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::use_result(): mysqli_result|false
```

Процедурний стиль

```methodsynopsis
mysqli_use_result(mysqli $mysql): mysqli_result|false
```

Используется для подготовки к использованию результирующего набора последнего запроса, запущенного функцией[mysqli\_real\_query()](mysqli.real-query.md)

Щоб результати запиту стали доступними, після запиту необхідно викликати або цю функцію, або [mysqli\_store\_result()](mysqli.store-result.md). Також виклик будь-якому з них запобігатиме відмову наступних запитів на цьому ж з'єднанні.

> **Зауваження** :
> 
> **mysqli\_use\_result()** не передає весь результуючий набір на клієнта, а отже, неможливо скористатися функцією [mysqli\_data\_seek()](mysqli-result.data-seek.md)для переміщення по ньому. Для цього потрібно скористатися функцією [mysqli\_store\_result()](mysqli.store-result.md). . **mysqli\_use\_result()** не слід використовувати, якщо на стороні клієнта дані результуючого набору довго обробляються, оскільки це затримує роботу сервера і не дає іншим процесам оновлювати таблиці, дані з яких є в результуючому наборі.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає небуферизований об'єкт результату запиту або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Пример #1 Пример использования**mysqli::use\_result()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query  = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполняем мультизапрос */
if ($mysqli->multi_query($query)) {
    do {
        /* получаем первый результирующий набор */
        if ($result = $mysqli->use_result()) {
            while ($row = $result->fetch_row()) {
                printf("%s\n", $row[0]);
            }
            $result->close();
        }
        /* печатаем разделитель */
        if ($mysqli->more_results()) {
            printf("-----------------\n");
        }
    } while ($mysqli->next_result());
}

/* закрываем соединение */
$mysqli->close();
?>
```

Процедурний стиль

```php
<?php
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

/* проверка соединения */
if (mysqli_connect_errno()) {
    printf("Не удалось подключиться: %s\n", mysqli_connect_error());
    exit();
}

$query  = "SELECT CURRENT_USER();";
$query .= "SELECT Name FROM City ORDER BY ID LIMIT 20, 5";

/* выполняем мультизапрос */
if (mysqli_multi_query($link, $query)) {
    do {
        /* получаем первый результирующий набор */
        if ($result = mysqli_use_result($link)) {
            while ($row = mysqli_fetch_row($result)) {
                printf("%s\n", $row[0]);
            }
            mysqli_free_result($result);
        }
        /* печатаем разделитель */
        if (mysqli_more_results($link)) {
            printf("-----------------\n");
        }
    } while (mysqli_next_result($link));
}

/* закрываем соединение */
mysqli_close($link);
?>
```

Результат виконання наведених прикладів:

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

-   [mysqli\_real\_query()](mysqli.real-query.md) \- Виконання SQL запиту
-   [mysqli\_store\_result()](mysqli.store-result.md) \- передає на клієнта результуючий набір останнього запиту
