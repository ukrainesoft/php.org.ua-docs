---
navigation:
  - function.pg-fetch-assoc.md: « pg\_fetch\_assoc
  - function.pg-fetch-result.md: pg\_fetch\_result »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_fetch\_object
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_fetch\_object

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_fetch\_object — Виберіть рядок результату запиту та повертає дані у вигляді об'єкта.

### Опис

```methodsynopsis
pg_fetch_object(    PgSql\Result $result,    ?int $row = null,    string $class = "stdClass",    array $constructor_args = []): object|false
```

**pg\_fetch\_object()** повертає об'єкт, властивості якого відповідають іменам полів вибірки. Також функція може створити екземпляр конкретного класу та передати параметри його конструктору.

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

За швидкістю функція ідентична [pg\_fetch\_array()](function.pg-fetch-array.md) і трохи повільніше [pg\_fetch\_row()](function.pg-fetch-row.md) (Різниця незначна).

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено або дорівнює **`null`**, береться наступний по черзі рядок.

`class`

Ім'я класу об'єкта, що створюється і повертається. Якщо не встановлено, функція створить екземпляр класу [stdClass](class.stdclass.md)

`constructor_args`

Необов'язковий аргумент. Масив (array) параметрів передачі в конструктор створюваного об'єкта (`class`

### Значення, що повертаються

Об'єкт (object), імена та значення властивостей якого відповідають іменам та значенням полів результату запиту. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, когда`row` перевищує кількість рядків у результаті запиту, коли рядків у результаті не залишилося, та за інших помилок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання** pg\_fetch\_object()\*\*\*\*

```php
<?php

$database = "store";

$db_conn = pg_connect("host=localhost port=5432 dbname=$database");
if (!$db_conn) {
  echo "Невозможно соединиться с базой postgres $database\n";
  exit;
}

$qu = pg_query($db_conn, "SELECT * FROM books ORDER BY author");


while ($data = pg_fetch_object($qu)) {
  echo $data->author . " (";
  echo $data->year . "): ";
  echo $data->title . "<br />";
}

pg_free_result($qu);
pg_close($db_conn);

?>
```

### Дивіться також

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_fetch\_array()](function.pg-fetch-array.md) \- Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_assoc()](function.pg-fetch-assoc.md) \- Вибирає рядок результату запиту та поміщає дані до асоціативного масиву
-   [pg\_fetch\_row()](function.pg-fetch-row.md) \- Вибирає рядок результату запиту та поміщає дані до масиву
-   [pg\_fetch\_result()](function.pg-fetch-result.md) \- Повертає запис із результату запиту
