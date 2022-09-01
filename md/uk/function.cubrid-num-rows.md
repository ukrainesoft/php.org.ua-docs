---
navigation:
  - function.cubrid-num-cols.html: « cubridnumcols
  - function.cubrid-pconnect-with-url.html: cubridpconnectwithurl »
  - index.md: PHP Manual
  - ref.cubrid.md: Функции CUBRID
title: cubridnumrows
---
# cubridnumrows

(PECL CUBRID >= 8.3.0)

cubridnumrows — Отримати кількість рядків у наборі результатів

### Опис

```methodsynopsis
cubrid_num_rows(resource $result): int
```

Функція **cubridnumrows()** використовується для одержання кількості рядків результату запиту. Може використовуватись для операторів `SELECT`. Для запитів `INSERT` `UPDATE` або `DELETE`, використовуйте функцію [cubridaffectedrows()](function.cubrid-affected-rows.md)

Примітка: Функцію **cubridnumrows()** можна використовувати лише для синхронного запиту; функція повертає 0, якщо використовується для асинхронного запиту.

### Список параметрів

`result`

`result` із виклику функцій [cubridexecute()](function.cubrid-execute.html) [cubridquery()](function.cubrid-query.html) і [cubridprepare()](function.cubrid-prepare.md)

### Значення, що повертаються

Кількість рядків у разі успішного виконання процесу.

0, якщо запит було здійснено в асинхронному режимі.

1, якщо SQL-оператор не є SELECT.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridnumrows()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb", "dba");

$req = cubrid_execute($conn, "SELECT * FROM code");

$row_num = cubrid_num_rows($req);
$col_num = cubrid_num_cols($req);

printf("Количество строк: %d\nКоличество столбцов: %d\n", $row_num, $col_num);

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
-   [cubridnumcols()](function.cubrid-num-cols.md) - Повертає кількість стовпців у наборі результатів
-   [cubridaffectedrows()](function.cubrid-affected-rows.md) - Кількість рядків, порушених останнім SQL-запитом
