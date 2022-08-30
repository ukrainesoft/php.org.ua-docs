Запускає попередньо підготовлений SQL-запит і передає параметри; не чекає результату, що повертається

-   [« pgselect](function.pg-select.html)
    
-   [пгsendprepare »](function.pg-send-prepare.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Запускає попередньо підготовлений SQL-запит і передає параметри; не чекає результату, що повертається
    

# пгsendexecute

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгsendexecute - Запускає попередньо підготовлений SQL-запит і передає йому параметри; не чекає результату, що повертається

### Опис

```methodsynopsis
pg_send_execute(PgSql\Connection $connection, string $statement_name, array $params): int|bool
```

Запускає попередньо підготовлений SQL-запит і передає параметри; не чекає результату, що повертається.

Працює аналогічно до функцій [пгsendqueryparams()](function.pg-send-query-params.html), тільки замість рядка із запитом приймає ім'я попередньо підготовленого SQL-запиту. Аргументи функції обробляються так само, як і функції [пгexecute()](function.pg-execute.html). Як і [пгexecute()](function.pg-execute.html) ця функція не працюватиме на з'єднаннях з серверами PostgreSQL версій нижче 7.4.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

`statement_name`

Ім'я підготовленого до виконання запиту. Якщо передано порожній рядок "", буде виконано безіменний запит. Ім'я та вміст запиту мають бути підготовлені функцією [пгprepare()](function.pg-prepare.html) [пгsendprepare()](function.pg-send-prepare.html) або за допомогою SQL-команди `PREPARE`

`params`

Масив значень параметрів запиту для заміни псевдозмінних $1, $2 і т.д. у вихідному рядку запиту. Кількість елементів масиву має точно збігатися з кількістю псевдозмінних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, **`false`** або `0` у разі виникнення помилки. Для отримання результату запиту скористайтеся функцією [пгgetresult()](function.pg-get-result.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгsendexecute()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Could not connect");

  // Подготовка запроса
  if (!pg_connection_busy($dbconn)) {
    pg_send_prepare($dbconn, "my_query", 'SELECT * FROM shops WHERE name = $1');
    $res1 = pg_get_result($dbconn);
  }

  // Запуск запроса на выполнение. Стоит отметить, что нет необходимости экранировать
  // спецсимволы в строке "Joe's Widgets"
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Joe's Widgets"));
    $res2 = pg_get_result($dbconn);
  }

  // Запуск на выполнение того же запроса, но с другим параметром
  if (!pg_connection_busy($dbconn)) {
    pg_send_execute($dbconn, "my_query", array("Clothes Clothes Clothes"));
    $res3 = pg_get_result($dbconn);
  }

?>
```

### Дивіться також

-   [пгprepare()](function.pg-prepare.html) - Надсилає запит на створення параметризованого SQL виразу і чекає на його завершення
-   [пгsendprepare()](function.pg-send-prepare.html) - Надсилає запит на створення параметризованого SQL-виразу, не чекаючи його завершення
-   [пгexecute()](function.pg-execute.html) - Запускає виконання раніше підготовленого параметризованого запиту та чекає результату