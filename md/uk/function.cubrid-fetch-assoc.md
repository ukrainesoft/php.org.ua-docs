- [«cubrid_fetch_array](function.cubrid-fetch-array.md)
- [cubrid_fetch_field »](function.cubrid-fetch-field.md)

- [PHP Manual](index.md)
- [Функції сумісності CUBRID MySQL](cubridmysql.cubrid.md)
- Витягти рядок із результуючого набору у вигляді асоціативного
масиву

#cubrid_fetch_assoc

(PECL CUBRID = 8.3.0)

cubrid_fetch_assoc — Витягти рядок з результуючого набору у вигляді
асоціативного масиву

### Опис

**cubrid_fetch_assoc**(resource `$result`, int `$type` = ?): array

Функція повертає асоціативний масив, що відповідає рядку в
результуючому наборі, на яку вказує внутрішній покажчик. Після
вилучення внутрішній покажчик переміщується на наступний рядок. Якщо
рядки закінчилися, то функція поверне **`false`**.

### Список параметрів

`result`
`Result`, отриманий з [cubrid_execute()](function.cubrid-execute.md)

`type`
Можливо тільки CUBRID_LOB. Цей параметр використовується лише якщо вам
необхідно оперувати об'єктами LOB.

### Значення, що повертаються

Асоціативний масив у разі успішного виконання.

**`false`**, якщо рядків більше немає; **`null`**, коли процес
завершується з помилкою.

### Приклади

**Приклад #1 Приклад використання **cubrid_fetch_assoc()****

` <?php$conn = cubrid_connect("localhost", 33000, "demodb");$req = cubrid_execute($conn, "SELECT name,area,seats,address FROM stadium WHERE    );printf("%-40s %-10s %-6s %-20s
", "name", "area", "seats", "address");while($row = cubrid_fetch_assoc($req)) {    printf("%-40s %-10s %-6s %-2
",        $row["name"], $row["area"], $row["seats"], $row["address"]);}//Якщо вам потрібно оперувати об'єктами LOB - | $req, CUBRID_LOB)cubrid_close_request($req);cubrid_disconnect($conn);?> `

Результат виконання цього прикладу:

name area seats address
Panathinaiko Stadium 86300.00 50000 Athens, Greece
Olympic Stadium 54700.00 13000 Athens, Greece
Olympic Indoor Hall 34100.00 18800 Athens, Greece
Olympic Hall 52400.00 21000 Athens, Greece
Olympic Aquatic Centre 42500.00 11500 Athens, Greece
Markopoulo Olympic Equestrian Centre 64000.00 15000 Markopoulo, Athens, Greece
Faliro Coastal Zone Olympic Complex 34650.00 12171 Faliro, Athens, Greece
Athens Olympic Stadium 120400.00 71030 Maroussi, Athens, Greece
Ano Liossia 34000.00 12000 Ano Liosia, Athens, Greece

### Дивіться також

- [cubrid_execute()](function.cubrid-execute.md) - Виконує
підготовлений SQL-оператор
- [cubrid_fetch()](function.cubrid-fetch.md) - Вибирає наступну
рядок із набору результатів
- [cubrid_fetch_row()](function.cubrid-fetch-row.md) - Вийняти
рядок із результуючого набору у вигляді індексованого масиву
- [cubrid_fetch_array()](function.cubrid-fetch-array.md) -
Вилучення рядка з результуючого набору у вигляді асоціативного
масиву, індексованого масиву або обох відразу
- [cubrid_fetch_object()](function.cubrid-fetch-object.md) - Вийняти
наступний рядок як об'єкт
