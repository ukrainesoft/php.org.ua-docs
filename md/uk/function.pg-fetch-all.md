---
navigation:
  - function.pg-fetch-all-columns.md: « pg\_fetch\_all\_columns
  - function.pg-fetch-array.md: pg\_fetch\_array »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_fetch\_all
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_fetch\_all

(PHP 4 >= 4.3.0, PHP 5, PHP 7, PHP 8)

pg\_fetch\_all — Вибирає всі дані з результату запиту та поміщає їх у масив

### Опис

```methodsynopsis
pg_fetch_all(PgSql\Result $result, int $mode = PGSQL_ASSOC): array
```

**pg\_fetch\_all()** повертає масив містить всі записи примірника [PgSql\\Result](class.pgsql-result.md)

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`** і **`PGSQL_BOTH`**При использовании**`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Багатовимірний масив даних результату запиту. Кожен рядок результату є масивом значень полів, індексованим іменами цих полів.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |
| 8.0.0 | Функция**pg\_fetch\_all()** тепер повертає порожній масив (array) замість значення **`false`** для наборів результатів без рядків. |
| 7.1.0 | Добавлен параметр`mode` |

### Приклади

**Приклад #1 Приклад використання**

```php
<?php
$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
    echo "Произошла ошибка.\n";
    exit;
}

$result = pg_query($conn, "SELECT * FROM authors");
if (!$result) {
    echo "Произошла ошибка.\n";
    exit;
}

$arr = pg_fetch_all($result);

print_r($arr);

?>
```

Висновок наведеного прикладу буде схожим на:

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

-   [pg\_fetch\_row()](function.pg-fetch-row.md) \- Вибирає рядок результату запиту та поміщає дані до масиву
-   [pg\_fetch\_array()](function.pg-fetch-array.md) \- Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.md) \- Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_fetch\_result()](function.pg-fetch-result.md) \- Повертає запис із результату запиту
