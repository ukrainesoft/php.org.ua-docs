---
navigation:
  - function.cubrid-next-result.md: « cubridnextresult
  - function.cubrid-num-rows.md: cubridnumrows »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridnumcols
---
# cubridnumcols

(PECL CUBRID >= 8.3.0)

cubridnumcols — Повертає кількість стовпців у наборі результатів

### Опис

```methodsynopsis
cubrid_num_cols(resource $result): int
```

Функція **cubridnumcols()** використовується для отримання кількості стовпців із результату запиту. Її можна використовувати тільки в тому випадку, якщо запит, що виконується, є оператором `SELECT`

### Список параметрів

`result`

Результат.

### Значення, що повертаються

Кількість стовпців у разі успішного виконання.

**`false`**, якщо SQL-вираз не є SELECT.

### Приклади

**Приклад #1 Приклад використання **cubridnumcols()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code");

$row_num = cubrid_num_rows($req);
$col_num = cubrid_num_cols($req);

printf("Количество строк: %d\nКоличество столбцов: %d\n", $row_num, $col_num);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
Количество строк: 6
Количество столбцов: 2
```

### Дивіться також

-   [cubridexecute()](function.cubrid-execute.md) - Виконує підготовлений SQL-оператор
-   [cubridnumrows()](function.cubrid-num-rows.md) - Отримати кількість рядків у наборі результатів
