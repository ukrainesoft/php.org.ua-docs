Запускає виконання раніше підготовленого параметризованого запиту та чекає результату

-   [« pg\_escape\_string](function.pg-escape-string.html)
    
-   [pg\_fetch\_all\_columns »](function.pg-fetch-all-columns.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
    

# пгexecute

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгexecute — Запускає виконання раніше підготовленого параметризованого запиту та чекає на результат

### Опис

```methodsynopsis
pg_execute(PgSql\Connection $connection = ?, string $stmtname, array $params): PgSql\Result|false
```

Запускає виконання раніше підготовленого параметризованого запиту та чекає на результат.

**пгexecute()** аналог функції [pg\_query\_params()](function.pg-query-params.html), тільки замість рядка із запитом приймає ім'я попередньо підготовленого SQL-запиту. Це дозволяє багаторазово виконувати один раз створені запити з різними параметрами. Сам запит має бути заздалегідь підготовлений у поточній сесії . **пгexecute()** підтримується PostgreSQL версії 7.4 та вище. Функція не працюватиме на з'єднаннях із сервером ранніх версій.

Аргументи функції ті ж, що й у [pg\_query\_params()](function.pg-query-params.html), за винятком імені попередньо складеного запиту, який передається замість рядка із запитом.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.html). Якщо `connection` не вказано, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [pg\_connect()](function.pg-connect.html) або [pg\_pconnect()](function.pg-pconnect.html)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`stmtname`

Ім'я підготовленого до виконання запиту. Якщо передано порожній рядок "", буде виконано безіменний запит. Ім'я та вміст запиту мають бути підготовлені функцією [pg\_prepare()](function.pg-prepare.html) [pg\_send\_prepare()](function.pg-send-prepare.html) або за допомогою SQL-команди `PREPARE`

`params`

Масив значень параметрів запиту для заміни псевдозмінних $1, $2 і т.д. у вихідному рядку запиту. Кількість елементів масиву має точно збігатися з кількістю псевдозмінних.

**Увага**

Елементи масиву будуть перетворені на рядки.

### Значення, що повертаються

Екземпляр [PgSql\\Result](class.pgsql-result.html) у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Повертає екземпляр [PgSql\\Result](class.pgsql-result.html); раніше повертався ресурс ([resource](language.types.resource.html) |
|  | Параметр `connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгexecute()****

```php
<?php
// Подключение к базе данных "mary"
$dbconn = pg_connect("dbname=mary");

// Подготовка запроса
$result = pg_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');

// Запуск запроса на выполнение. Стоит отметить, что нет необходимости экранировать
// спецсимволы в строке "Joe's Widgets"
$result = pg_execute($dbconn, "my_query", array("Joe's Widgets"));

// Запуск на выполнение того же запроса, но с другим параметром
$result = pg_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));

?>
```

### Дивіться також

-   [pg\_prepare()](function.pg-prepare.html) - Надсилає запит на створення параметризованого SQL виразу і чекає на його завершення
-   [pg\_send\_prepare()](function.pg-send-prepare.html) - Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення
-   [pg\_query\_params()](function.pg-query-params.html) - Надсилає параметризований запит на сервер, параметри передаються окремо від тексту SQL запиту