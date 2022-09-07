---
navigation:
  - function.cubrid-fetch-array.md: « cubridfetcharray
  - function.cubrid-fetch-field.md: cubridfetchfield »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubridfetchassoc
---
# cubridfetchassoc

(PECL CUBRID >= 8.3.0)

cubridfetchassoc — Витягти рядок із результуючого набору у вигляді асоціативного масиву

### Опис

```methodsynopsis
cubrid_fetch_assoc(resource $result, int $type = ?): array
```

Функція повертає асоціативний масив, відповідному рядку в результуючому наборі, на яку вказує внутрішній покажчик. Після вилучення внутрішній покажчик переміщується на наступний рядок. Якщо рядки закінчилися, то функція поверне **`false`**

### Список параметрів

`result`

`Result`, отриманий з [cubridexecute()](function.cubrid-execute.md)

`type`

Можливо тільки CUBRIDLOB. Цей параметр використовується лише якщо вам потрібно оперувати об'єктами LOB.

### Значення, що повертаються

Асоціативний масив у разі успішного виконання.

\*\*`false`\*\*якщо рядків більше немає; \*\*`null`\*\*коли процес завершується з помилкою.

### Приклади

**Приклад #1 Приклад використання **cubridfetchassoc()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT name,area,seats,address FROM stadium WHERE nation_code='GRE' AND seats > 10000");

printf("%-40s %-10s %-6s %-20s\n", "name", "area", "seats", "address");
while ($row = cubrid_fetch_assoc($req)) {
    printf("%-40s %-10s %-6s %-20s\n",
        $row["name"], $row["area"], $row["seats"], $row["address"]);
}

// Если вам нужно оперировать объектами LOB - используйте
// cubrid_fetch_assoc($req, CUBRID_LOB)

cubrid_close_request($req);

cubrid_disconnect($conn);
?>
```

Результат виконання цього прикладу:

```
name                                     area       seats  address
Panathinaiko Stadium                     86300.00   50000  Athens, Greece
Olympic Stadium                          54700.00   13000  Athens, Greece
Olympic Indoor Hall                      34100.00   18800  Athens, Greece
Olympic Hall                             52400.00   21000  Athens, Greece
Olympic Aquatic Centre                   42500.00   11500  Athens, Greece
Markopoulo Olympic Equestrian Centre     64000.00   15000  Markopoulo, Athens, Greece
Faliro Coastal Zone Olympic Complex      34650.00   12171  Faliro, Athens, Greece
Athens Olympic Stadium                   120400.00  71030  Maroussi, Athens, Greece
Ano Liossia                              34000.00   12000  Ano Liosia, Athens, Greece
```

### Дивіться також

-   [cubridexecute()](function.cubrid-execute.md) - Виконує підготовлений SQL-оператор
-   [cubridfetch()](function.cubrid-fetch.md) - Вибирає наступний рядок із набору результатів
-   [cubridfetchrow()](function.cubrid-fetch-row.md) - Витягти рядок із результуючого набору у вигляді індексованого масиву
-   [cubridfetcharray()](function.cubrid-fetch-array.md) - Вилучення рядка з результуючого набору у вигляді асоціативного масиву, індексованого масиву або обох відразу
-   [cubridfetchobject()](function.cubrid-fetch-object.md) - Витягти наступний рядок як об'єкт
