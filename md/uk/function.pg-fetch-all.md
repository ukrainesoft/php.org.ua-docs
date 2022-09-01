---
navigation:
  - function.pg-fetch-all-columns.html: « pgfetchallcolumns
  - function.pg-fetch-array.html: пгfetcharray »
  - index.md: PHP Manual
  - ref.pgsql.md: Функции PostgreSQL
title: пгfetchall
---
# пгfetchall

(PHP 4> = 4.3.0, PHP 5, PHP 7, PHP 8)

пгfetchall — Вибирає всі дані з результату запиту та поміщає їх у масив

### Опис

```methodsynopsis
pg_fetch_all(PgSql\Result $result, int $mode = PGSQL_ASSOC): array
```

**пгfetchall()** повертає масив містить всі записи примірника [PgSqlResult](class.pgsql-result.md)

> **Зауваження**: Ця функція встановлює NULL-поля значення **`null`** PHP.

### Список параметрів

`result`

Екземпляр [PgSqlResult](class.pgsql-result.html), що повертається функціями [пгquery()](function.pg-query.html) [пгqueryparams()](function.pg-query-params.html) або [пгexecute()](function.pg-execute.md) (між іншим).

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`** і **`PGSQL_BOTH`**. При використанні **`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Багатовимірний масив даних результату запиту. Кожен рядок результату є масивом значень полів, індексованим іменами цих полів.

### список змін

| Версия | Описание |
| --- | --- |
|  | Параметр `result` тепер чекає екземпляр [PgSqlResult](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
|  | Функція **пгfetchall()** тепер повертає порожній масив (array) замість значення **`false`** для наборів результатів без рядків. |
|  | Доданий параметр `mode` |

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
    echo "Произошла ошибка.\n";
    exit;
}

$result = pg_query($conn, "SELECT * FROM authors");
if (!$result) {
    echo "Произошла ошибка.\n";
    exit;
}

$arr = pg_fetch_all($result);

print_r($arr);

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Array
(
    [0] => Array
        (
            [id] => 1
            [name] => Fred
        )

    [1] => Array
        (
            [id] => 2
            [name] => Bob
        )

)
```

### Дивіться також

-   [пгfetchrow()](function.pg-fetch-row.md) - Вибирає рядок результату запиту та поміщає дані до масиву
-   [пгfetcharray()](function.pg-fetch-array.md) - Повертає рядок результату у вигляді масиву
-   [пгfetchobject()](function.pg-fetch-object.md) - Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [пгfetchresult()](function.pg-fetch-result.md) - Повертає запис із результату запиту
