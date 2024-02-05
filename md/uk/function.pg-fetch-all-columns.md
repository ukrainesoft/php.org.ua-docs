---
navigation:
  - function.pg-execute.md: « pg\_execute
  - function.pg-fetch-all.md: pg\_fetch\_all »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_fetch\_all\_columns
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_fetch\_all\_columns

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

pg\_fetch\_all\_columns — Вибирає всі записи з однієї колонки результату запиту та поміщає їх у масив

### Опис

```methodsynopsis
pg_fetch_all_columns(PgSql\Result $result, int $field = 0): array
```

**pg\_fetch\_all\_columns()** повертає масив, що містить усі записи однієї колонки екземпляра [PgSql\\Result](class.pgsql-result.md)

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`field`

Номер колонки. Якщо параметр не заданий, буде оброблено першу (нульову) колонку.

### Значення, що повертаються

Масив значень стовпчика результату запиту.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_fetch\_all\_columns()\*\*\*\*

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT title, name, address FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

// Получить массив имён всех авторов
$arr = pg_fetch_all_columns($result, 1);

var_dump($arr);

?>
```

### Дивіться також

-   [pg\_fetch\_all()](function.pg-fetch-all.md) \- Вибирає всі дані з результату запиту та поміщає їх у масив
