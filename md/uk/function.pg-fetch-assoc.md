---
navigation:
  - function.pg-fetch-array.html: « pgfetcharray
  - function.pg-fetch-object.html: пгfetchobject »
  - index.html: PHP Manual
  - ref.pgsql.html: Функции PostgreSQL
title: пгfetchassoc
---
# пгfetchassoc

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгfetchassoc - Вибирає рядок результату запиту і поміщає дані в асоціативний масив

### Опис

```methodsynopsis
pg_fetch_assoc(PgSql\Result $result, ?int $row = null): array|false
```

**пгfetchassoc()** повертає асоціативний масив, що містить запис з рядка результату запиту.

Результат виконання **пгfetchassoc()** той самий, що й у [пгfetcharray()](function.pg-fetch-array.html) з параметром **`PGSQL_ASSOC`**. Функція повертає лише асоціативний масив. Якщо потрібний чисельно-індексований масив, використовуйте функцію [пгfetchrow()](function.pg-fetch-row.html)

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

**пгfetchassoc()** не набагато повільніше і значно простіше у використанні, ніж [пгfetchrow()](function.pg-fetch-row.html)

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено або дорівнює **`null`**, береться наступний по черзі рядок.

### Значення, що повертаються

Асоціативний масив індексований іменами полів вибірки. Значення масиву представляються як текстових рядків. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, якщо `row` перевищує кількість рядків у результаті запиту, коли рядків у результаті не залишилося, та за інших помилок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.html) |

### Приклади

**Приклад #1 Приклад використання **пгfetchassoc()****

```php
<?php
$conn = pg_connect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT id, author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

while ($row = pg_fetch_assoc($result)) {
  echo $row['id'];
  echo $row['author'];
  echo $row['email'];
}
?>
```

### Дивіться також

-   [пгfetchrow()](function.pg-fetch-row.html) - Вибирає рядок результату запиту та поміщає дані до масиву
-   [пгfetcharray()](function.pg-fetch-array.html) - Повертає рядок результату у вигляді масиву
-   [пгfetchobject()](function.pg-fetch-object.html) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгfetchresult()](function.pg-fetch-result.html) - Повертає запис із результату запиту
