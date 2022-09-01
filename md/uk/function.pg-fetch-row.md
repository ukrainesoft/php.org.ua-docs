---
navigation:
  - function.pg-fetch-result.html: « pgfetchresult
  - function.pg-field-is-null.html: пгfieldісnull »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfetchrow
---
# пгfetchrow

(PHP 4, PHP 5, PHP 7, PHP 8)

пгfetchrow — Вибирає рядок результату запиту та поміщає дані до масиву

### Опис

```methodsynopsis
pg_fetch_row(PgSql\Result $result, ?int $row = null, int $mode = PGSQL_NUM): array|false
```

**пгfetchrow()** вибирає один рядок із результату запиту `result`

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.html) (між іншим).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено або дорівнює **`null`**, береться наступний по черзі рядок.

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`** і **`PGSQL_BOTH`**. При використанні **`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Чисельно індексований масив значень рядка результату запиту. Індексація починається із нуля. Значення подаються у вигляді рядків. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, якщо `row` перевищує кількість рядків у результаті запиту, коли рядків у результаті не залишилося, та за інших помилок.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.html); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Приклад #1 Приклад використання **пгfetchrow()****

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

while ($row = pg_fetch_row($result)) {
  echo "Автор: $row[0]  E-mail: $row[1]";
  echo "<br />\n";
}

?>
```

### Дивіться також

-   [пгquery()](function.pg-query.html) - Виконує запит
-   [пгfetcharray()](function.pg-fetch-array.html) - Повертає рядок результату у вигляді масиву
-   [пгfetchobject()](function.pg-fetch-object.html) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгfetchresult()](function.pg-fetch-result.html) - Повертає запис із результату запиту
