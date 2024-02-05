---
navigation:
  - function.mysql-ping.md: « mysql\_ping
  - function.mysql-real-escape-string.md: mysql\_real\_escape\_string »
  - index.md: PHP Manual
  - ref.mysql.md: MySQL
title: mysql\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysql\_query

(PHP 4, PHP 5)

mysql\_query — Надсилає запит MySQL

**Увага**

Цей модуль застарів, починаючи з версії PHP 5.5.0, і видалений у PHP 7.0.0. Використовуйте замість нього [MySQLi](book.mysqli.md) або [PDO\_MySQL](ref.pdo-mysql.md)Смотрите также инструкцию[MySQL: вибір API](mysqlinfo.api.choosing.md). Альтернативи для цієї функції:

-   [mysqli\_query()](mysqli.query.md)
-   [PDO::query()](pdo.query.md)

### Опис

```methodsynopsis
mysql_query(string $query, resource $link_identifier = NULL): mixed
```

**mysql\_query()** посилає один запит (надсилання кількох запитів не підтримується) активній базі даних сервера, на який посилається переданий дескриптор `link_identifier`

### Список параметрів

`query`

SQL-запит

Запит не повинен закінчуватися крапкою з комою. Дані у запиті мають бути [коректно проекрановано](function.mysql-real-escape-string.md)

`link_identifier`

З'єднання MySQL. Якщо ідентифікатор з'єднання не вказано, буде використано останнє з'єднання, відкрите [mysql\_connect()](function.mysql-connect.md). Якщо таке з'єднання не було знайдено, функція спробує створити таке, якби [mysql\_connect()](function.mysql-connect.md) було викликано без параметрів. Якщо з'єднання не було знайдено та не змогло бути створено, генерується помилка рівня **`E_WARNING`**

### Значення, що повертаються

Для запитів SELECT, SHOW, DESCRIBE, EXPLAIN та інших запитів, що повертають результат з кількох рядів, **mysql\_query()** повертає дескриптор результату запиту (resource), або \*\*`false`\*\*в случае возникновения ошибки.

Для інших типів SQL-запитів, INSERT, UPDATE, DELETE, DROP та інших, **mysql\_query()** повертає **`true`** у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

Отриманий дескриптор результату слід передати у функцію [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md)или любую другую функцию, работающую с результатами запросов.

Используйте[mysql\_num\_rows()](function.mysql-num-rows.md) для з'ясування кількості рядів в результаті SELECT-запиту або [mysql\_affected\_rows()](function.mysql-affected-rows.md) для з'ясування кількості опрацьованих рядів запитами DELETE, INSERT, REPLACE та UPDATE.

**mysql\_query()** також завершиться з помилкою та поверне **`false`**, якщо користувач не має доступу до будь-якої з таблиць, що фігурують у запиті.

### Приклади

**Приклад #1 Неправильний запит**

Следующий запрос составлен неправильно и**mysql\_query()** поверне **`false`**

```php
<?php
$result = mysql_query('SELECT * WHERE 1 = 1');
if (!$result) {
    die('Неверный запрос: ' . mysql_error());
}

?>
```

**Приклад #2 Вірний запит**

Наступний запит вірний, тому **mysql\_query()** поверне ресурс.

```php
<?php
// Эти данные, к примеру, могли быть получены от пользователя
$firstname = 'fred';
$lastname  = 'fox';

// Формируем запрос
// Это лучший способ выполнить SQL-запрос
// Ещё примеры можно найти в документации mysql_real_escape_string()
$query = sprintf("SELECT firstname, lastname, address, age FROM friends
    WHERE firstname='%s' AND lastname='%s'",
    mysql_real_escape_string($firstname),
    mysql_real_escape_string($lastname));

// Выполняем запрос
$result = mysql_query($query);

// Проверяем результат
// Это показывает реальный запрос, посланный к MySQL, а также ошибку. Удобно при отладке.
if (!$result) {
    $message  = 'Неверный запрос: ' . mysql_error() . "\n";
    $message .= 'Запрос целиком: ' . $query;
    die($message);
}

// Используем результат
// Попытка напечатать $result не выведет информацию, которая в нем хранится
// Необходимо использовать какую-либо mysql-функцию, работающую с результатом запроса
// Смотрите также mysql_result(), mysql_fetch_array(), mysql_fetch_row() и т.п.
while ($row = mysql_fetch_assoc($result)) {
    echo $row['firstname'];
    echo $row['lastname'];
    echo $row['address'];
    echo $row['age'];
}

// Освобождаем ресурсы, ассоциированные с результатом
// Это делается автоматически в конце скрипта
mysql_free_result($result);
?>
```

### Дивіться також

-   [mysql\_connect()](function.mysql-connect.md) \- Відкриває з'єднання із сервером MySQL
-   [mysql\_error()](function.mysql-error.md) \- Повертає текст помилки останньої операції з MySQL
-   [mysql\_real\_escape\_string()](function.mysql-real-escape-string.md) \- Екранує спеціальні символи у рядках для використання у виразах SQL
-   [mysql\_result()](function.mysql-result.md) \- Повертає дані результату запиту
-   [mysql\_fetch\_assoc()](function.mysql-fetch-assoc.md) \- Повертає ряд результату запиту як асоціативний масив.
-   [mysql\_unbuffered\_query()](function.mysql-unbuffered-query.md) \- Надсилає запит MySQL без авто-обробки результату та його буферизації
