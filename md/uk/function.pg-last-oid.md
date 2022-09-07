---
navigation:
  - function.pg-last-notice.md: « pglastnotice
  - function.pg-lo-close.md: пглоclose »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгlastoid
---
# пгlastoid

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгlastoid — Повертає OID останнього доданого до бази рядка

### Опис

```methodsynopsis
pg_last_oid(PgSql\Result $result): string|int|false
```

**пгlastoid()** використовується для визначення OID, що відповідає вставленому в таблицю рядку.

Поле OID таблиць баз даних стало необов'язковим, починаючи з версії PostgreSQL 7.2, а з версії 8.1 перестане додаватися до таблиць за замовчуванням. Якщо поле OID таблиці не встановлено, використовуйте функцію [пгresultstatus()](function.pg-result-status.md) для перевірки успішності вставлення записів у таблицю.

Щоб отримати значення `SERIAL` поля після вставки рядка в таблицю, використовуйте функцію PostgreSQL `CURRVAL`, Передавши їй ім'я послідовності, значення якої потрібно отримати. Щоб дізнатися про ім'я послідовності, необхідно використовувати функцію `pg_get_serial_sequence` (PostgreSQL 8.0).

У PostgreSQL 8.1 є функція `LASTVAL`, що повертає значення найчастіше використовуваної за сесію послідовності. Так можна уникнути необхідність задавати назву послідовності, таблиці чи колонки.

> **Зауваження**
> 
> Колишня назва функції: **пгgetlastoid()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

### Значення, що повертаються

Ціле число (int) або рядок (string), що містить OID останнього вставленого рядка на з'єднанні `connection`, або **`false`**, якщо помилка або поле OID недоступне.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгlastoid()****

```php
<?php
  // Подключение к базе данных
  pg_connect("dbname=mark host=localhost");

  // Создание тестовой таблицы
  pg_query("CREATE TABLE test (a INTEGER) WITH OIDS");

  // Вставка данных в таблицу
  $res = pg_query("INSERT INTO test VALUES (1)");

  $oid = pg_last_oid($res);
?>
```

### Дивіться також

-   [пгquery()](function.pg-query.md) - Виконує запит
-   [пгresultstatus()](function.pg-result-status.md) - Повертає стан результату запиту
