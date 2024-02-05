---
navigation:
  - function.pg-trace.md: « pg\_trace
  - function.pg-tty.md: pg\_tty »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_transaction\_status
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_transaction\_status

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_transaction\_status — Повертає поточний стан транзакції на сервері

### Опис

```methodsynopsis
pg_transaction_status(PgSql\Connection $connection): int
```

Повертає стан транзакції на сервері.

**Застереження**

**pg\_transaction\_status()** видає некоректний результат під час роботи з сервером PostgreSQL 7.3, на якому вимкнено опцію `autocommit`. Автоматичне завершення транзакцій на стороні сервера застаріло і не використовується у пізніших версіях.

### Список параметрів

`connection`

Екземпляр [PgSql\\Connection](class.pgsql-connection.md)

### Значення, що повертаються

Список можливих станів: **`PGSQL_TRANSACTION_IDLE`** (сервер не діє), **`PGSQL_TRANSACTION_ACTIVE`** (виконується запит), **`PGSQL_TRANSACTION_INTRANS`** (сервер не діє, робота в режимі транзакції), або **`PGSQL_TRANSACTION_INERROR`** (сервер не діє, транзакція зазнала невдачі) . **`PGSQL_TRANSACTION_UNKNOWN`**\- ошибка подключения**`PGSQL_TRANSACTION_ACTIVE`** повертається лише коли запит вже надіслано на сервер, але ще не оброблено.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`connection` тепер чекає екземпляр [PgSql\\Connection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_transaction\_status()\*\*\*\*

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Подключиться не удалось");
  $stat = pg_transaction_status($dbconn);
  if ($stat === PGSQL_TRANSACTION_UNKNOWN) {
      echo 'Соединение не удалось';
  } else if ($stat === PGSQL_TRANSACTION_IDLE) {
      echo 'Соединение свободно и простаивает';
  } else {
      echo 'Соединение в режиме транзакции';
  }
?>
```
