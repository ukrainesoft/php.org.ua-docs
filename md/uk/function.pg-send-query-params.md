Посилає параметризований запит на сервер, не чекає результату, що повертається.

-   [« pgsendprepare](function.pg-send-prepare.html)
    
-   [пгsendquery »](function.pg-send-query.html)
    
-   [PHP Manual](index.html)
    
-   [Функции PostgreSQL](ref.pgsql.html)
    
-   Посилає параметризований запит на сервер, не чекає результату, що повертається.
    

# пгsendqueryparams

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгsendqueryparams — Посилає параметризований запит на сервер, не чекає результату, що повертається.

### Опис

```methodsynopsis
pg_send_query_params(PgSql\Connection $connection, string $query, array $params): int|bool
```

Надсилає параметризований запит на виконання і не чекає на його завершення. Параметри передаються окремо від тексту запиту SQL.

Функція є аналогом [пгsendquery()](function.pg-send-query.html) за одним винятком: параметри запиту можна надсилати окремо від рядка запиту. Аргументи функції обробляються так само, як і в [пгqueryparams()](function.pg-query-params.html). . [пгsendquery()](function.pg-send-query.html) підтримується на з'єднаннях із серверами PostgreSQL версій 7.4 та вище. Функція не працюватиме із серверами ранніх версій. Також вона підтримує лише одну SQL-команду у виразі.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.html)

`query`

Параметризований запит SQL. Повинен містити лише один вираз (кілька виразів розділених крапкою з комою не підтримуються). Якщо в запит будуть передаватися параметри, вони замінять псевдозмінні $1, $2 і т.д.

`params`

Масив значень параметрів запиту для заміни псевдозмінних $1, $2 і т.д. у вихідному рядку запиту. Кількість елементів масиву має точно збігатися з кількістю псевдозмінних.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання, **`false`** або `0` у разі виникнення помилки. Для отримання результату запиту скористайтеся функцією [пгgetresult()](function.pg-get-result.html)

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгsendqueryparams()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Не удалось подключиться");

  // Использование параметров. Стоит заметить, что нет необходимости
  // заключать в кавычки и экранировать параметр.
  pg_send_query_params($dbconn, 'select count(*) from authors where city = $1', array('Perth'));

  // В сравнении с pg_send_query
  $str = pg_escape_string('Perth');
  pg_send_query($dbconn, "select count(*) from authors where city = '${str}'");
?>
```

### Дивіться також

-   [пгsendquery()](function.pg-send-query.html) - Надсилає асинхронний запит