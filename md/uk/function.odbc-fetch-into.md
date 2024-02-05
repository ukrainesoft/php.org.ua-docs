---
navigation:
  - function.odbc-fetch-array.md: « odbc\_fetch\_array
  - function.odbc-fetch-object.md: odbc\_fetch\_object »
  - index.md: PHP Manual
  - ref.uodbc.md: Функції ODBC
title: odbc\_fetch\_into
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# odbc\_fetch\_into

(PHP 4, PHP 5, PHP 7, PHP 8)

odbc\_fetch\_into — Повертає один рядок результату до масиву

### Опис

```methodsynopsis
odbc_fetch_into(resource $statement, array &$array, int $row = 0): int|false
```

Повертає один рядок результату масив (array).

### Список параметрів

`statement`

Ресурс результату.

`array`

Масив результатів (array) може бути будь-якого типу, оскільки він буде перетворений на масив типів. Він міститиме значення стовпців, починаючи з індексу 0.

`row`

Номер рядка.

### Значення, що повертаються

Повертає кількість стовпців у результаті; \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклади використання **odbc\_fetch\_into()****

```php
<?php
$rc = odbc_fetch_into($res_id, $my_array);
?>
```

або

```php
<?php
$rc = odbc_fetch_into($res_id, $my_array, 2);
?>
```
