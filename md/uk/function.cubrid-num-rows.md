---
navigation:
  - function.cubrid-num-cols.md: « cubrid\_num\_cols
  - function.cubrid-pconnect-with-url.md: cubrid\_pconnect\_with\_url »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_num\_rows
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_num\_rows

(PECL CUBRID >= 8.3.0)

cubrid\_num\_rows — Отримати кількість рядків у наборі результатів

### Опис

```methodsynopsis
cubrid_num_rows(resource $result): int
```

Функция**cubrid\_num\_rows()** використовується для одержання кількості рядків результату запиту. Може використовуватись для операторів `SELECT`. Для запитів `INSERT` `UPDATE`или`DELETE`, используйте функцию[cubrid\_affected\_rows()](function.cubrid-affected-rows.md)

Примечание: Функцию**cubrid\_num\_rows()** можна використовувати лише для синхронного запиту; функція повертає 0, якщо використовується для асинхронного запиту.

### Список параметрів

`result`

`result` із виклику функцій [cubrid\_execute()](function.cubrid-execute.md) [cubrid\_query()](function.cubrid-query.md) і [cubrid\_prepare()](function.cubrid-prepare.md)

### Значення, що повертаються

Кількість рядків у разі успішного виконання процесу.

0, якщо запит було здійснено в асинхронному режимі.

\-1, якщо SQL-оператор не є SELECT.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** cubrid\_num\_rows()\*\*\*\*

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

Результат виконання наведеного прикладу:

```
Количество строк: 6
Количество столбцов: 2
```

### Дивіться також

-   [cubrid\_execute()](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
-   [cubrid\_num\_cols()](function.cubrid-num-cols.md) \- Повертає кількість стовпців у наборі результатів
-   [cubrid\_affected\_rows()](function.cubrid-affected-rows.md) \- Кількість рядків, порушених останнім SQL-запитом
