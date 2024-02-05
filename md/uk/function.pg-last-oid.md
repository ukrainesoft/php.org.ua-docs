---
navigation:
  - function.pg-last-notice.md: « pg\_last\_notice
  - function.pg-lo-close.md: pg\_lo\_close »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_last\_oid
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_last\_oid

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_last\_oid — Повертає OID останнього доданого до бази рядка

### Опис

```methodsynopsis
pg_last_oid(PgSql\Result $result): string|int|false
```

**pg\_last\_oid()** використовується для визначення OID, що відповідає вставленому в таблицю рядку.

Поле OID таблиць баз даних стало необов'язковим, починаючи з версії PostgreSQL 7.2, а з версії 8.1 перестане додаватися до таблиць за замовчуванням. Якщо поле OID таблиці не встановлено, використовуйте функцію [pg\_result\_status()](function.pg-result-status.md) для перевірки успішності вставлення записів у таблицю.

Щоб отримати значення `SERIAL`поля после вставки строки в таблицу, используйте функцию PostgreSQL`CURRVAL`, Передавши їй ім'я послідовності, значення якої потрібно отримати. Щоб дізнатися про ім'я послідовності, необхідно використовувати функцію `pg_get_serial_sequence`(PostgreSQL 8.0).

У PostgreSQL 8.1 є функція `LASTVAL`, що повертає значення найчастіше використовуваної за сесію послідовності. Так можна уникнути необхідність задавати назву послідовності, таблиці чи колонки.

> **Зауваження** :
> 
> Прежнее название функции:**pg\_getlastoid()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

### Значення, що повертаються

Ціле число (int) або рядок (string), що містить OID останнього вставленого рядка на з'єднанні `connection`, либо\*\*`false`\*\*, якщо помилка або поле OID недоступне.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_last\_oid()\*\*\*\*

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

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_result\_status()](function.pg-result-status.md) \- Повертає стан результату запиту
