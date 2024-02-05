---
navigation:
  - function.pg-socket.md: « pg\_socket
  - function.pg-transaction-status.md: pg\_transaction\_status »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_trace
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_trace

(PHP 4 >= 4.0.1, PHP 5, PHP 7, PHP 8)

pg\_trace — Включає трасування підключення PostgreSQL

### Опис

```methodsynopsis
pg_trace(    string $filename,    string $mode = "w",    ?PgSql\Connection $connection = null,    int $trace_mode = 0): bool
```

**pg\_trace()** включає трасування з'єднання з PostgreSQL сервером у зовнішній файл. Щоб розуміти вміст таких файлів, необхідно добре розумітися на внутрішньому пристрої клієнт-серверної взаємодії.

Для тих, хто не володіє подібними навичками, трасування все ж таки може виявитися корисним для пошуку помилок при відправці запитів на сервер. Наприклад, можна виконати команду **grep '^To backend' trace.log** та подивитися, які запити реально надіслані на сервер. Додаткову інформацію можна отримати з [» документації PostgreSQL](http://www.postgresql.org/docs/current/interactive/)

### Список параметрів

`filename`

Повний шлях та ім'я файлу для запису журналу трасування. Аналогічно [fopen()](function.fopen.md)

`mode`

Необов'язковий аргумент. Режим доступу до файлу. Аналогічно [fopen()](function.fopen.md)

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md). Якщо параметр `connection`указан как\*\*`null`\*\*, вибирається стандартне з'єднання. Стандартне з'єднання — це останнє з'єднання, яке встановила функція [pg\_connect()](function.pg-connect.md) або [pg\_pconnect()](function.pg-pconnect.md)

**Увага**

Починаючи з версії PHP 8.1.0, використання стандартного з'єднання застаріло.

`trace_mode`

Необов'язковий режим трасування з наступними константами: **`PGSQL_TRACE_SUPPRESS_TIMESTAMPS`**и**`PGSQL_TRACE_REGRESS_MODE`**

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.3.0 | Добавлен параметр`trace_mode` |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | `connection` тепер допускає значення null. |

### Приклади

**Пример #1 Пример использования**pg\_trace()\*\*\*\*

```php
<?php
$pgsql_conn = pg_connect("dbname=mark host=localhost");

if ($pgsql_conn) {
   pg_trace('/tmp/trace.log', 'w', $pgsql_conn);
   pg_query("SELECT 1");
   pg_untrace($pgsql_conn);
   // Теперь /tmp/trace.log будет хранить информацию о взаимодействии с сервером
} else {
   print pg_last_error($pgsql_conn);
   exit;
}
?>
```

### Дивіться також

-   [fopen()](function.fopen.md) \- Відкриває файл або URL
-   [pg\_untrace()](function.pg-untrace.md) \- Вимикає трасування з'єднання з PostgreSQL
