Опитування підключень

-   [« mysqli::ping](mysqli.ping.html)
    
-   [mysqli::prepare »](mysqli.prepare.html)
    
-   [PHP Manual](index.html)
    
-   [mysqli](class.mysqli.html)
    
-   Опитування підключень
    

# mysqli::poll

# mysqlipoll

(PHP 5> = 5.3.0, PHP 7, PHP 8)

mysqli::poll -- mysqlipoll — Опитування підключень

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public static mysqli::poll(    ?array &$read,    ?array &$error,    array &$reject,    int $seconds,    int $microseconds = 0): int|false
```

Процедурний стиль

```methodsynopsis
mysqli_poll(    ?array &$read,    ?array &$error,    array &$reject,    int $seconds,    int $microseconds = 0): int|false
```

Опитування підключень. Метод може використовуватись як [статичний](language.oop5.static.html)

> **Зауваження**
> 
> Доступно лише з модулем [mysqlnd](book.mysqlnd.html)

### Список параметрів

`read`

Список з'єднань для перевірки наявності результатів, які можна прочитати.

`error`

Список з'єднань, на яких відбулися помилки, наприклад, не вдався запит або з'єднання було втрачено.

`reject`

Список з'єднань, які були відхилені, тому що на них не було запущено асинхронний запит, з яким функція може отримати результат опитування.

`seconds`

Максимальна кількість секунд очікування має бути невід'ємною.

`microseconds`

Максимальна кількість мілісекунд очікування має бути невід'ємною.

### Значення, що повертаються

Повертає кількість готових до роботи з'єднань у разі успішного виконання, **`false`** у разі невдачі.

### Приклади

**Приклад #1 Приклад використання **mysqlipoll()****

```php
<?php
$link1 = mysqli_connect();
$link1->query("SELECT 'test'", MYSQLI_ASYNC);
$all_links = array($link1);
$processed = 0;
do {
    $links = $errors = $reject = array();
    foreach ($all_links as $link) {
        $links[] = $errors[] = $reject[] = $link;
    }
    if (!mysqli_poll($links, $errors, $reject, 1)) {
        continue;
    }
    foreach ($links as $link) {
        if ($result = $link->reap_async_query()) {
            print_r($result->fetch_row());
            if (is_object($result))
                mysqli_free_result($result);
        } else die(sprintf("Ошибка MySQLi: %s", mysqli_error($link)));
        $processed++;
    }
} while ($processed < count($all_links));
?>
```

Результат виконання цього прикладу:

```
Array
(
    [0] => test
)
```

### Дивіться також

-   [mysqliquery()](mysqli.query.html) - Виконує запит до бази даних
-   [mysqlireapasyncquery()](mysqli.reap-async-query.html) - Отримання результату асинхронного запиту