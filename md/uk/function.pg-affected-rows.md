---
navigation:
  - ref.pgsql.md: « Функції PostgreSQL
  - function.pg-cancel-query.md: pg\_cancel\_query »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_affected\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_affected\_rows

(PHP 4 >= 4.2.0, PHP 5, PHP 7, PHP 8)

pg\_affected\_rows — Повертає кількість порушених запитом записів (кортежів)

### Опис

```methodsynopsis
pg_affected_rows(PgSql\Result $result): int
```

**pg\_affected\_rows()** повертає кількість кортежів (сутностей/записів/рядів) порушених запитом `INSERT` `UPDATE`, и`DELETE`queries.

З версії PostgreSQL 9.0 і більше, сервер повертає кількість вибраних рядів для запиту SELECT. Старіші версії повертають 0 для SELECT.

> **Зауваження** :
> 
> Раніше ця функція називалася **pg\_cmdtuples()**

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

### Значення, що повертаються

Кількість записів, порушених запитом. Якщо жоден кортеж не торкнувся, функція поверне

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_affected\_rows()\*\*\*\*

```php
<?php
$result = pg_query($conn, "INSERT INTO authors VALUES ('Orwell', 2002, 'Animal Farm')");

$cmdtuples = pg_affected_rows($result);

echo $cmdtuples . " кортежей затронуто.\n";
?>
```

Результат виконання наведеного прикладу:

```
1 кортежей затронуто.
```

### Дивіться також

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_query\_params()](function.pg-query-params.md) \- Надсилає параметризований запит на сервер, параметри передаються окремо від тексту SQL запиту
-   [pg\_execute()](function.pg-execute.md) \- Запускає виконання раніше підготовленого параметризованого запиту та чекає результату
-   [pg\_num\_rows()](function.pg-num-rows.md) \- Повертає кількість рядків у вибірці
