---
navigation:
  - ref.pgsql.md: « Функции PostgreSQL
  - function.pg-cancel-query.md: пгcancelquery »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгaffectedrows
---
# пгaffectedrows

(PHP 4> = 4.2.0, PHP 5, PHP 7, PHP 8)

пгaffectedrows — Повертає кількість порушених запитом записів (кортежів)

### Опис

```methodsynopsis
pg_affected_rows(PgSql\Result $result): int
```

**пгaffectedrows()** повертає кількість кортежів (сутностей/записів/рядів) порушених запитом `INSERT` `UPDATE`, і `DELETE` queries.

З версії PostgreSQL 9.0 і більше, сервер повертає кількість вибраних рядів для запиту SELECT. Старіші версії повертають 0 для SELECT.

> **Зауваження**
> 
> Раніше ця функція називалася **пгcmdtuples()**

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.md), що повертається функціями [пгquery()](function.pg-query.md) [пгqueryparams()](function.pg-query-params.md) або [пгexecute()](function.pg-execute.md) (між іншим).

### Значення, що повертаються

Кількість записів, порушених запитом. Якщо жоден кортеж не торкнувся, функція поверне `0`

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгaffectedrows()****

```php
<?php
$result = pg_query($conn, "INSERT INTO authors VALUES ('Orwell', 2002, 'Animal Farm')");

$cmdtuples = pg_affected_rows($result);

echo $cmdtuples . " кортежей затронуто.\n";
?>
```

Результат виконання цього прикладу:

```
1 кортежей затронуто.
```

### Дивіться також

-   [пгquery()](function.pg-query.md) - Виконує запит
-   [пгqueryparams()](function.pg-query-params.md) - Надсилає параметризований запит на сервер, параметри передаються окремо від тексту SQL запиту
-   [пгexecute()](function.pg-execute.md) - Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
-   [пгnumrows()](function.pg-num-rows.md) - Повертає кількість рядків у вибірці
