---
navigation:
  - function.cubrid-error.md: « cubriderror
  - function.cubrid-fetch-assoc.md: cubridfetchassoc »
  - index.md: PHP Manual
  - cubridmysql.cubrid.md: Функції сумісності CUBRID MySQL
title: cubridfetcharray
---
# cubridfetcharray

(PECL CUBRID >=8.3.0)

cubridfetcharray - Вилучення рядка з результуючого набору у вигляді асоціативного масиву, індексованого масиву або обох відразу

### Опис

```methodsynopsis
cubrid_fetch_array(resource $result, int $type = CUBRID_BOTH): array
```

Функція **cubridfetcharray()** служить для отримання одного рядка з результуючого набору. Після вилучення курсор автоматично пересунеться на наступний рядок.

### Список параметрів

`result`

`Result` отриманий з [cubridexecute()](function.cubrid-execute.md)

`type`

Тип масиву для вилучення: CUBRIDNUM, CUBRIDASSOC, CUBRIDBOTH. Якщо вам потрібно оперувати об'єктами типу LOB – використовуйте CUBRIDЛОБ.

### Значення, що повертаються

Повертає масив рядків, що відповідає вилученому рядку, у разі успішного виконання.

\*\*`false`\*\*якщо рядків більше немає; NULL, коли процес завершується помилкою.

Тип масива, що повертається, залежить від заданого типу. За замовчуванням використовується CUBRIDBOTH, що веде до вилучення як асоціативного, і індексованого масивів, але це поведінка можна перевизначити параметром `type`. Значення, допустимі для параметра `type`

-   CUBRIDNUM: Індексований масив (перший елемент має індекс 0)
-   CUBRIDASSOC : Асоціативний масив
-   CUBRIDBOTH : І той і інший одночасно (за замовчуванням)

### Приклади

**Приклад #1 Приклад використання **cubridfetcharray()****

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT name,area,seats,address FROM stadium WHERE nation_code='GRE' AND seats > 10000");

printf("%-40s %-10s %-6s %-20s\n", "name", "area", "seats", "address");
while ($row = cubrid_fetch_array($req, CUBRID_NUM)) {
    printf("%-40s %-10s %-6s %-20s\n", $row[0], $row[1], $row[2], $row[3]);
}

// Если вам нужно оперировать объектами LOB - используйте
// cubrid_fetch_array($req, CUBRID_NUM | CUBRID_LOB)

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
-   [cubridfetchassoc()](function.cubrid-fetch-assoc.md) - Витягти рядок із результуючого набору у вигляді асоціативного масиву
-   [cubridfetchobject()](function.cubrid-fetch-object.md) - Витягти наступний рядок як об'єкт
