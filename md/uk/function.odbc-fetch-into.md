---
navigation:
  - function.odbc-fetch-array.html: « odbcfetcharray
  - function.odbc-fetch-object.html: odbcfetchobject »
  - index.html: PHP Manual
  - ref.uodbc.html: Функции ODBC
title: odbcfetchinto
---
# odbcfetchinto

(PHP 4, PHP 5, PHP 7, PHP 8)

odbcfetchinto — Повертає один рядок результату до масиву

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

Повертає кількість стовпців у результаті; **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклади використання **odbcfetchinto()****

```php
<?php
$rc = odbc_fetch_into($res_id, $my_array);
?>
```

або

```php
<?php
$rc = odbc_fetch_into($res_id, $my_array, 2);
?>
```
