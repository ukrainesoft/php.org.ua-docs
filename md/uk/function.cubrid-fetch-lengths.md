---
navigation:
  - function.cubrid-fetch-field.md: « cubrid\_fetch\_field
  - function.cubrid-fetch-object.md: cubrid\_fetch\_object »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_fetch\_lengths
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_fetch\_lengths

(PECL CUBRID >= 8.3.0)

cubrid\_fetch\_lengths - Повертає масив, що містить довжини всіх стовпців поточного рядка

### Опис

```methodsynopsis
cubrid_fetch_lengths(resource $result): array
```

Функція повертає індексований масив, що містить довжини стовпців у поточному рядку з результуючого набору, або \*\*`false`\*\*в случае возникновения ошибки.

> **Зауваження** :
> 
> Якщо стовпець типу BLOB/CLOB, то для отримання його довжини використовуйте [cubrid\_lob\_size()](function.cubrid-lob-size.md)

### Список параметрів

`result`

`Result` отриманий з [cubrid\_execute()](function.cubrid-execute.md)

### Значення, що повертаються

Індексований масив.

\*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**cubrid\_fetch\_lengths()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$row = cubrid_fetch_row($result);
print_r($row);

$lens = cubrid_fetch_lengths($result);
print_r($lens);

cubrid_disconnect($conn);
?>
```

Результат виконання наведеного прикладу:

```
Array
(
    [0] => 2004
    [1] => 20085
    [2] => 15118
    [3] => 30134
    [4] => AUS
    [5] => G
    [6] => 2004-8-20
)
Array
(
    [0] => 4
    [1] => 5
    [2] => 5
    [3] => 5
    [4] => 3
    [5] => 1
    [6] => 10
)
```
