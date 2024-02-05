---
navigation:
  - function.pg-escape-string.md: « pg\_escape\_string
  - function.pg-fetch-all-columns.md: pg\_fetch\_all\_columns »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_execute
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_execute

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_execute — Запускає виконання раніше підготовленого параметризованого запиту та чекає на результат

### Опис

```methodsynopsis
pg_execute(PgSql\Connection $connection = ?, string $stmtname, array $params): PgSql\Result|false
```

Запускає виконання раніше підготовленого параметризованого запиту та чекає на результат.

**pg\_execute()** аналог функції [pg\_query\_params()](function.pg-query-params.md), тільки замість рядка із запитом приймає ім'я попередньо підготовленого SQL-запиту. Це дозволяє багаторазово виконувати один раз створені запити з різними параметрами. Сам запит має бути заздалегідь підготовлений у поточній сесії . **pg\_execute()** підтримується PostgreSQL версії 7.4 та вище. Функція не працюватиме на з'єднаннях із сервером ранніх версій.

Аргументи функції ті ж, що й у [pg\_query\_params()](function.pg-query-params.md), за винятком імені попередньо складеного запиту, який передається замість рядка із запитом.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection` не вказано, буде вибрано стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`stmtname`

Ім'я підготовленого до виконання запиту. Якщо передано порожній рядок "", буде виконано безіменний запит. Ім'я та вміст запиту мають бути підготовлені функцією [pg\_prepare()](function.pg-prepare.md) [pg\_send\_prepare()](function.pg-send-prepare.md) або за допомогою SQL-команди `PREPARE`

`params`

Масив значень параметрів запиту для заміни псевдозмінних $1, $2 і т.д. у вихідному рядку запиту. Кількість елементів масиву має точно збігатися з кількістю псевдозмінних.

**Увага**

Елементи масиву будуть перетворені на рядки.

### Значення, що повертаються

Екземпляр [PgSql\\Result](class.pgsql-result.md) у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Повертає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше повертався ресурс ([resource](language.types.resource.md) |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_execute()\*\*\*\*

```php
<?php
// Подключение к базе данных "mary"
$dbconn = pg_connect("dbname=mary");

// Подготовка запроса
$result = pg_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');

// Запуск запроса на выполнение. Стоит отметить, что нет необходимости экранировать
// спецсимволы в строке "Joe's Widgets"
$result = pg_execute($dbconn, "my_query", array("Joe's Widgets"));

// Запуск на выполнение того же запроса, но с другим параметром
$result = pg_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));

?>
```

### Дивіться також

-   [pg\_prepare()](function.pg-prepare.md) \- Надсилає запит на створення параметризованого SQL виразу і чекає на його завершення
-   [pg\_send\_prepare()](function.pg-send-prepare.md) \- Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення
-   [pg\_query\_params()](function.pg-query-params.md) \- Надсилає параметризований запит на сервер, параметри передаються окремо від тексту SQL запиту
