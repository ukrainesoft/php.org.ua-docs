---
navigation:
  - function.pg-fetch-array.md: « pg\_fetch\_array
  - function.pg-fetch-object.md: pg\_fetch\_object »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_fetch\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_fetch\_assoc

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_fetch\_assoc - Вибирає рядок результату запиту і поміщає дані в асоціативний масив

### Опис

```methodsynopsis
pg_fetch_assoc(PgSql\Result $result, ?int $row = null): array|false
```

**pg\_fetch\_assoc()** повертає асоціативний масив, що містить запис з рядка результату запиту.

Результат виконання **pg\_fetch\_assoc()** той самий, що й у [pg\_fetch\_array()](function.pg-fetch-array.md)с параметром\*\*`PGSQL_ASSOC`\*\*. Функція повертає лише асоціативний масив. Якщо потрібний чисельно-індексований масив, використовуйте функцію [pg\_fetch\_row()](function.pg-fetch-row.md)

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

**pg\_fetch\_assoc()** не набагато повільніше і значно простіше у використанні, ніж [pg\_fetch\_row()](function.pg-fetch-row.md)

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено або дорівнює **`null`**, береться наступний по черзі рядок.

### Значення, що повертаються

Асоціативний масив індексований іменами полів вибірки. Значення масиву представляються як текстових рядків. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, якщо `row` перевищує кількість рядків у результаті запиту, коли рядків у результаті не залишилося, та за інших помилок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_fetch\_assoc()\*\*\*\*

```php
<?php
$conn = pg_connect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT id, author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

while ($row = pg_fetch_assoc($result)) {
  echo $row['id'];
  echo $row['author'];
  echo $row['email'];
}
?>
```

### Дивіться також

-   [pg\_fetch\_row()](function.pg-fetch-row.md) \- Вибирає рядок результату запиту та поміщає дані до масиву
-   [pg\_fetch\_array()](function.pg-fetch-array.md) \- Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.md) \- Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_fetch\_result()](function.pg-fetch-result.md) \- Повертає запис із результату запиту
