---
navigation:
  - function.pg-fetch-result.md: « pg\_fetch\_result
  - function.pg-field-is-null.md: pg\_field\_is\_null »
  - index.md: PHP Manual
  - ref.pgsql.md: Функції PostgreSQL
title: pg\_fetch\_row
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# pg\_fetch\_row

(PHP 4, PHP 5, PHP 7, PHP 8)

pg\_fetch\_row — Вибирає рядок результату запиту та поміщає дані до масиву

### Опис

```methodsynopsis
pg_fetch_row(PgSql\Result $result, ?int $row = null, int $mode = PGSQL_NUM): array|false
```

**pg\_fetch\_row()** вибирає один рядок із результату запиту `result`

> **Зауваження**: Ця функція встановлює NULL-поля значення \*\*`null`\*\*PHP.

### Список параметрів

`result`

Екземпляр [PgSql\\Result](class.pgsql-result.md), що повертається функціями [pg\_query()](function.pg-query.md) [pg\_query\_params()](function.pg-query-params.md) або [pg\_execute()](function.pg-execute.md)(среди прочего).

`row`

Номер вибирається з результату запиту рядка. Нумерація починається із нуля. Якщо аргумент опущено або дорівнює **`null`**, береться наступний по черзі рядок.

`mode`

Необов'язковий параметр, керуючий тим, як індексується масив, що повертається (array). Параметр `mode` є константою і може приймати такі значення: **`PGSQL_ASSOC`** **`PGSQL_NUM`**и**`PGSQL_BOTH`**При использовании**`PGSQL_NUM`** функція повертає масив із числовими індексами, при використанні **`PGSQL_ASSOC`** вона поверне лише асоціативні індекси, а **`PGSQL_BOTH`** поверне як числові, і асоціативні індекси.

### Значення, що повертаються

Чисельно індексований масив значень рядка результату запиту. Індексація починається із нуля. Значення подаються у вигляді рядків. Значення `NULL` бази даних перетворюються на PHP **`null`**

**`false`**, якщо `row` перевищує кількість рядків у результаті запиту, коли рядків у результаті не залишилося, та за інших помилок.

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Параметр`result` тепер чекає екземпляр [PgSql\\Result](class.pgsql-result.md); раніше очікувався ресурс ([resource](language.types.resource.md) |

### Приклади

**Пример #1 Пример использования**pg\_fetch\_row()\*\*\*\*

```php
<?php

$conn = pg_pconnect("dbname=publisher");
if (!$conn) {
  echo "Произошла ошибка.\n";
  exit;
}

$result = pg_query($conn, "SELECT author, email FROM authors");
if (!$result) {
  echo "Произошла ошибка.\n";
  exit;
}

while ($row = pg_fetch_row($result)) {
  echo "Автор: $row[0]  E-mail: $row[1]";
  echo "<br />\n";
}

?>
```

### Дивіться також

-   [pg\_query()](function.pg-query.md) \- Виконує запит
-   [pg\_fetch\_array()](function.pg-fetch-array.md) \- Повертає рядок результату у вигляді масиву
-   [pg\_fetch\_object()](function.pg-fetch-object.md) \- Вибирає рядок результату запиту та повертає дані у вигляді об'єкта
-   [pg\_fetch\_result()](function.pg-fetch-result.md) \- Повертає запис із результату запиту
