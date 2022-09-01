---
navigation:
  - function.pg-trace.html: « pgtrace
  - function.pg-tty.html: пгtty »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгtransactionstatus
---
# пгtransactionstatus

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгtransactionstatus — Повертає поточний стан транзакції на сервері

### Опис

```methodsynopsis
pg_transaction_status(PgSql\Connection $connection): int
```

Повертає стан транзакції на сервері.

**Застереження**

**пгtransactionstatus()** видає некоректний результат під час роботи з сервером PostgreSQL 7.3, на якому вимкнено опцію `autocommit`. Автоматичне завершення транзакцій на стороні сервера застаріло і не використовується у пізніших версіях.

### Список параметрів

`connection`

Екземпляр [PgSqlConnection](class.pgsql-connection.md)

### Значення, що повертаються

Список можливих станів: **`PGSQL_TRANSACTION_IDLE`** (сервер не діє), **`PGSQL_TRANSACTION_ACTIVE`** (виконується запит), **`PGSQL_TRANSACTION_INTRANS`** (сервер не діє, робота в режимі транзакції), або **`PGSQL_TRANSACTION_INERROR`** (сервер не діє, транзакція зазнала невдачі) . **`PGSQL_TRANSACTION_UNKNOWN`** - помилка підключення . **`PGSQL_TRANSACTION_ACTIVE`** повертається лише коли запит вже надіслано на сервер, але ще не оброблено.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `connection` тепер чекає екземпляр [PgSqlConnection](class.pgsql-connection.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгtransactionstatus()****

```php
<?php
  $dbconn = pg_connect("dbname=publisher") or die("Подключиться не удалось");
  $stat = pg_transaction_status($dbconn);
  if ($stat === PGSQL_TRANSACTION_UNKNOWN) {
      echo 'Соединение не удалось';
  } else if ($stat === PGSQL_TRANSACTION_IDLE) {
      echo 'Соединение свободно и простаивает';
  } else {
      echo 'Соединение в режиме транзакции';
  }
?>
```
