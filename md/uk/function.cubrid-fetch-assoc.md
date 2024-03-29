---
navigation:
  - function.cubrid-fetch-array.md: « cubrid\_fetch\_array
  - function.cubrid-fetch-field.md: cubrid\_fetch\_field »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubrid\_fetch\_assoc
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_fetch\_assoc

(PECL CUBRID >= 8.3.0)

cubrid\_fetch\_assoc — Витягти рядок із результуючого набору у вигляді асоціативного масиву

### Опис

```methodsynopsis
cubrid_fetch_assoc(resource $result, int $type = ?): array
```

Функція повертає асоціативний масив, відповідному рядку в результуючому наборі, на яку вказує внутрішній покажчик. Після вилучення внутрішній покажчик переміщується на наступний рядок. Якщо рядки закінчилися, то функція поверне **`false`**

### Список параметрів

`result`

`Result`, отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`type`

Можливо тільки CUBRID\_LOB. Цей параметр використовується лише якщо вам потрібно оперувати об'єктами LOB.

### Значення, що повертаються

Асоціативний масив у разі успішного виконання.

\*\*`false`\*\*якщо рядків більше немає; \*\*`null`\*\*коли процес завершується з помилкою.

### Приклади

**Приклад #1 Приклад використання** cubrid\_fetch\_assoc()\*\*\*\*

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

Результат виконання наведеного прикладу:

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

-   [cubrid\_execute()](function.cubrid-execute.md) \- Виконує підготовлений SQL-оператор
-   [cubrid\_fetch()](function.cubrid-fetch.md) \- Вибирає наступний рядок із набору результатів
-   [cubrid\_fetch\_row()](function.cubrid-fetch-row.md) \- Витягти рядок із результуючого набору у вигляді індексованого масиву
-   [cubrid\_fetch\_array()](function.cubrid-fetch-array.md) \- Вилучення рядка з результуючого набору у вигляді асоціативного масиву, індексованого масиву або обох відразу
-   [cubrid\_fetch\_object()](function.cubrid-fetch-object.md) \- Витягти наступний рядок як об'єкт
