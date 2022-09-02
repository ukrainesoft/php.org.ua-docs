---
navigation:
  - function.pg-execute.md: « pgexecute
  - function.pg-fetch-all.md: пгfetchall »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfetchallcolumns
---
# пгfetchallcolumns

(PHP 5> = 5.1.0, PHP 7, PHP 8)

пгfetchallcolumns — Вибирає всі записи з однієї колонки результату запиту та поміщає їх у масив

### Опис

```methodsynopsis
pg_fetch_all_columns(PgSql\Result $result, int $field = 0): array
```

**пгfetchallcolumns()** повертає масив, що містить усі записи однієї колонки екземпляра [PgSqlResult](class.pgsql-result.md)

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

`field`

Номер колонки. Якщо параметр не заданий, буде оброблено першу (нульову) колонку.

### Значення, що повертаються

Масив значень стовпчика результату запиту.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгfetchallcolumns()****

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT title, name, address FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

// Получить Масив имён всех авторов
$arr = pg_fetch_all_columns($result, 1);

var_dump($arr);

?>
```

### Дивіться також

-   [пгfetchall()](function.pg-fetch-all.md) - Вибирає всі дані з результату запиту та поміщає їх у масив
