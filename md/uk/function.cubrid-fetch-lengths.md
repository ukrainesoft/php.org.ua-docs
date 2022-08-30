Повертає масив, що містить довжини всіх стовпців поточного рядка

-   [« cubridfetchfield](function.cubrid-fetch-field.html)
    
-   [cubridfetchobject »](function.cubrid-fetch-object.html)
    
-   [PHP Manual](index.html)
    
-   [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.html)
    
-   Повертає масив, що містить довжини всіх стовпців поточного рядка
    

# cubridfetchlengths

(PECL CUBRID >= 8.3.0)

cubridfetchlengths - Повертає масив, що містить довжини всіх стовпців поточного рядка

### Опис

```methodsynopsis
cubrid_fetch_lengths(resource $result): array
```

Функція повертає індексований масив, що містить довжини стовпців у поточному рядку з результуючого набору, або **`false`** у разі виникнення помилки.

> **Зауваження**
> 
> Якщо стовпець типу BLOB/CLOB, то для отримання його довжини використовуйте [cubridlobsize()](function.cubrid-lob-size.html)

### Список параметрів

`result`

`Result` отриманий з [cubridexecute()](function.cubrid-execute.html)

### Значення, що повертаються

Індексований масив.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubridfetchlengths()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND nation_code='AUS' AND medal='G'");

$row = cubrid_fetch_row($result);
print_r($row);

$lens = cubrid_fetch_lengths($result);
print_r($lens);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

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