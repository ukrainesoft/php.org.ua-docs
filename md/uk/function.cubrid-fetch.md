---
navigation:
  - function.cubrid-execute.md: « cubrid\_execute
  - function.cubrid-free-result.md: cubrid\_free\_result »
  - index.md: PHP Manual
  - ref.cubrid.md: Функції CUBRID
title: cubrid\_fetch
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# cubrid\_fetch

(PECL CUBRID >= 8.3.0)

cubrid\_fetch — Вибирає наступний рядок із набору результатів

### Опис

```methodsynopsis
cubrid_fetch(resource $result, int $type = CUBRID_BOTH): mixed
```

Функция**cubrid\_fetch()** використовується для отримання одного рядка результату запиту. Курсор автоматично переміститься на наступний рядок після отримання результату.

### Список параметрів

`result`

`result`, отриманий з [cubrid\_execute()](function.cubrid-execute.md)

`type`

Тип масиву отриманого результату CUBRID\_NUM, CUBRID\_ASSOC, CUBRID\_BOTH, CUBRID\_OBJECT. Для керування LOB-об'єктом використовуйте CUBRID\_LOB.

### Значення, що повертаються

Масив результатів або об'єкт у разі успішного виконання процесу.

\*\*`false`\*\*якщо рядків більше немає; NULL у разі виникнення помилки.

Результат може бути отриманий як масив, або як об'єкт, установка параметра `type` визначає, який тип даних використати. Змінною `type` можна присвоїти одне з наступних значень:

-   CUBRID\_NUM : Числовий масив (починаючи з 0)
-   CUBRID\_ASSOC : Асоціативний масив
-   CUBRID\_BOTH : Числовий & асоціативний масив (за замовчуванням)
-   CUBRID\_OBJECT : об'єкт, з іменем атрибута як ім'я стовпця результату запиту

Якщо параметр `type`опущен, результат будет получен с использованием опции CUBRID\_BOTH за замовчуванням. Для отримання результату запиту як об'єктних даних, ім'я стовпця результату має підпорядковуватися правилам іменування ідентифікаторів в PHP. Наприклад, ім'я стовпця, таке як "count(\*)", не може бути отримано у вигляді об'єкта.

### Приклади

**Приклад #1 Приклад використання** cubrid\_fetch()\*\*\*\*

```php
<?php
$conn = cubrid_connect("localhost", 33000, "demodb");
$req = cubrid_execute($conn, "SELECT * FROM stadium WHERE nation_code='GRE' AND seats > 10000");

printf("%-40s %-10s %-6s %-20s\n", "name", "area", "seats", "address");
while ($row = cubrid_fetch($req)) {
    printf("%-40s %-10s %-6s %-20s\n",
        $row["name"], $row["area"], $row["seats"], $row["address"]);
}

// для управления LOB-объектом, можно использовать cubrid_fetch($req, CUBRID_LOB)

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
-   [cubrid\_fetch\_array()](function.cubrid-fetch-array.md) \- Вилучення рядка з результуючого набору у вигляді асоціативного масиву, індексованого масиву або обох відразу
-   [cubrid\_fetch\_row()](function.cubrid-fetch-row.md) \- Витягти рядок із результуючого набору у вигляді індексованого масиву
-   [cubrid\_fetch\_assoc()](function.cubrid-fetch-assoc.md) \- Витягти рядок із результуючого набору у вигляді асоціативного масиву
-   [cubrid\_fetch\_object()](function.cubrid-fetch-object.md) \- Витягти наступний рядок як об'єкт
