---
navigation:
  - function.cubrid-next-result.md: « cubrid\_next\_result
  - function.cubrid-num-rows.md: cubrid\_num\_rows »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_num\_cols
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_num\_cols

(PECL CUBRID >= 8.3.0)

cubrid\_num\_cols — Повертає кількість стовпців у наборі результатів

### Опис

```methodsynopsis
cubrid_num_cols(resource $result): int
```

Функция**cubrid\_num\_cols()** використовується для отримання кількості стовпців із результату запиту. Її можна використовувати тільки в тому випадку, якщо запит, що виконується, є оператором `SELECT`

### Список параметрів

`result`

Результат.

### Значення, що повертаються

Кількість стовпців у разі успішного виконання.

**`false`**, якщо SQL-вираз не є SELECT.

### Приклади

**Пример #1 Пример использования**cubrid\_num\_cols()\*\*\*\*

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
-   [cubrid\_num\_rows()](function.cubrid-num-rows.md) \- Отримати кількість рядків у наборі результатів
