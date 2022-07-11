- [«cubrid_fetch_field](function.cubrid-fetch-field.md)
- [cubrid_fetch_object »](function.cubrid-fetch-object.md)

- [PHP Manual](index.md)
- [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
- Повертає масив, що містить довжини всіх стовпців поточного рядка

#cubrid_fetch_lengths

(PECL CUBRID = 8.3.0)

cubrid_fetch_lengths - Повертає масив, що містить довжини всіх стовпців
поточного рядка

### Опис

**cubrid_fetch_lengths**(resource `$result`): array

Функція повертає індексований масив, що містить довжини стовпців
поточному рядку з результуючого набору, або **`false`** у разі
виникнення помилки.

> **Примітка**:
>
> Якщо стовпець типу BLOB/CLOB, то для отримання його довжини використовуйте
> [cubrid_lob_size()](function.cubrid-lob-size.md).

### Список параметрів

`result`
`Result` отриманий з [cubrid_execute()](function.cubrid-execute.md)

### Значення, що повертаються

Індексований масив.

**`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **cubrid_fetch_lengths()****

` <?php$conn = cubrid_connect("localhost", 33000, "demodb");$result = cubrid_execute($conn, "SELECT * FROM game WHERE host_year=2004 AND' );$row = cubrid_fetch_row($result);print_r($row);$lens = cubrid_fetch_lengths($result);print_r($lens);cubrid_disconnect($conn);?> `

Результат виконання цього прикладу:

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
