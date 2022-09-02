---
navigation:
  - function.pg-socket.md: « pgsocket
  - function.pg-transaction-status.md: пгtransactionstatus »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгtrace
---
# пгtrace

(PHP 4> = 4.0.1, PHP 5, PHP 7, PHP 8)

пгtrace — Включає трасування підключення PostgreSQL

### Опис

```methodsynopsis
pg_trace(string $filename, string $mode = "w", ?PgSql\Connection $connection = null): bool
```

**пгtrace()** включає трасування з'єднання з PostgreSQL сервером у зовнішній файл. Щоб розуміти вміст таких файлів, необхідно добре розумітися на внутрішньому пристрої клієнт-серверної взаємодії.

Для тих, хто не володіє подібними навичками, трасування все ж таки може виявитися корисним для пошуку помилок при відправці запитів на сервер. Наприклад, можна виконати команду **grep '^To backend' trace.log** та подивитися, які запити реально надіслані на сервер. Додаткову інформацію можна отримати з [» документации PostgreSQL](http://www.postgresql.org/docs/current/interactive/)

### Список параметрів

`filename`

Повний шлях та ім'я файлу для запису журналу трасування. Аналогічно [fopen()](function.fopen.md)

`mode`

Необов'язковий аргумент. Режим доступу до файлу. Аналогічно [fopen()](function.fopen.md)

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md). Якщо параметр `connection` вказано **`null`**, використовується стандартне з'єднання. Стандартне з'єднання - це останнє з'єднання, виконане за допомогою функцій [пгconnect()](function.pg-connect.md) або [пгpconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | `connection` тепер допускає значення null. |

### Приклади

**Приклад #1 Приклад використання **пгtrace()****

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   pg_trace('/tmp/trace.log', 'w', $pgsql_conn);
   pg_query("SELECT 1");
   pg_untrace($pgsql_conn);
   // Теперь /tmp/trace.log будет хранить информацию о взаимодействии с сервером
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```

### Дивіться також

-   [fopen()](function.fopen.md) - Відкриває файл або URL
-   [пгuntrace()](function.pg-untrace.md) - Вимикає трасування з'єднання з PostgreSQL
