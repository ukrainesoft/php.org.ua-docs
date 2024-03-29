---
navigation:
  - function.cubrid-ping.md: « cubrid\_ping
  - function.cubrid-real-escape-string.md: cubrid\_real\_escape\_string »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_query
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_query

(PECL CUBRID >= 8.3.1)

cubrid\_query — Надсилання запиту CUBRID

### Опис

```methodsynopsis
cubrid_query(string $query, resource $conn_identifier = ?): resource
```

Функция**cubrid\_query()** посилає унікальний запит (множинні запити не підтримуються) поточної активної бази даних, заданої ідентифікатором з'єднання `conn_identifier`

### Список параметрів

`query`

SQL-запит

Дані у запиті мають бути [коректно екрановані](function.cubrid-real-escape-string.md)

`conn_identifier`

Ідентифікатор з'єднання. Якщо не встановлено, то буде використано останнє, відкрите за допомогою [cubrid\_connect()](function.cubrid-connect.md)соединение.

### Значення, що повертаються

Для SELECT, SHOW, DESCRIBE, EXPLAIN та інших запитів, що повертають результуючий набір, **cubrid\_query()** повертає resource у разі успішного виконання та \*\*`false`\*\*в случае возникновения ошибки.

Для інших типів SQL-запитів, INSERT, UPDATE, DELETE, DROP і т.д. **cubrid\_query()** повертає **`true`** або **`false`** залежно від успішності виконання.

Повернутий результат можна передавати у функцію [cubrid\_fetch\_array()](function.cubrid-fetch-array.md) і їй подібні до роботи з отриманими даними.

Используйте[cubrid\_num\_rows()](function.cubrid-num-rows.md) для визначення кількості повернутих оператором SELECT рядків або [cubrid\_affected\_rows()](function.cubrid-affected-rows.md) для визначення кількості порушених рядків, для запитів, що змінюють дані, таких як DELETE, INSERT, REPLACE та UPDATE.

**cubrid\_query()** також може завершитися з помилкою та повернути **`false`**, якщо користувач не має права на доступ до таблиці, яка використовується у запиті.

### Приклади

**Приклад #1 Некоректний запит**

Наступний запит містить синтаксичну помилку, тому **cubrid\_query()** поверне **`false`**

```php
<?php
$conn = cubrid_connect('localhost', 33000, 'demodb');

$result = cubrid_query('SELECT * WHERE 1=1');
if (!$result) {
    die('Некорректный запрос: ' . cubrid_error());
}

?>
```

**Приклад #2 Коректний запит**

Наступний запит коректний, тож **cubrid\_query()** поверне ресурс.

```php
<?php
// Какие нибудь значения
$firstname = 'fred';
$lastname  = 'fox';

$conn = cubrid_connect('localhost', 33000, 'demodb');

cubrid_execute($conn,"DROP TABLE if exists friends");
cubrid_execute($conn,"create table friends(firstname varchar,lastname varchar,address char(24),age int)");
cubrid_execute($conn,"insert into friends values('fred','fox','home-1','20')");
cubrid_execute($conn,"insert into friends values('blue','cat','home-2','21')");
// Сформулируем запрос
// Это лучший путь для выполнения запроса
// Другие Приклады смотрите cubrid_real_escape_string()
$query = sprintf("SELECT firstname, lastname, address, age FROM friends WHERE firstname='%s' AND lastname='%s'",
cubrid_real_escape_string($firstname),
cubrid_real_escape_string($lastname));

// Выполняем запрос
$result = cubrid_query($query);

// Проверяем результат
// Показывает сам запрос и ошибку. полезно при отладке.
if (!$result) {
    $message  = 'Некорректный запрос: ' . cubrid_error() . "\n";
    $message .= 'Всего запросов: ' . $query;
    die($message);
}

// Используем результат
// Попытка распечатать $result не позволит получить доступ к информации в ресурсе
// Должна быть использована одна из функций cubrid
// Смотрите cubrid_result(), cubrid_fetch_array(), cubrid_fetch_row() и т.д.
while ($row = cubrid_fetch_assoc($result)) {
    echo $row['firstname'];
    echo $row['lastname'];
    echo $row['address'];
    echo $row['age'];
}

// Освобождаем ресурсы. В принципе можно и не делать, так как
// они будут автоматически освобождены после завершения работы скрипта
cubrid_free_result($result);
?>
```

### Дивіться також

-   [cubrid\_connect()](function.cubrid-connect.md) \- Відкриває з'єднання з сервером CUBRID
-   [cubrid\_error()](function.cubrid-error.md) \- Повертає текст останньої помилки, що відбулася.
-   [cubrid\_real\_escape\_string()](function.cubrid-real-escape-string.md) \- Екранування спеціальних символів у SQL-запиті
-   [cubrid\_result()](function.cubrid-result.md) \- Отримати значення із заданого стовпця заданого рядка
-   [cubrid\_fetch\_assoc()](function.cubrid-fetch-assoc.md) \- Витягти рядок із результуючого набору у вигляді асоціативного масиву
-   [cubrid\_unbuffered\_query()](function.cubrid-unbuffered-query.md) \- Виконання запиту без завантаження результату на згадку
