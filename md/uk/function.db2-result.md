---
navigation:
  - function.db2-procedures.md: « db2\_procedures
  - function.db2-rollback.md: db2\_rollback »
  - index.md: PHP Manual
  - ref.ibm-db2.md: Функції IBM DB2
title: db2\_result
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# db2\_result

(PECL ibm\_db2 >= 1.0.0)

db2\_result — Повертає один стовпець із рядка у наборі результатів

### Опис

```methodsynopsis
db2_result(resource $stmt, int|string $column): ?mixed
```

Используйте**db2\_result()**, щоб повернути значення вказаного стовпця у поточному рядку набору результатів. Ви повинні викликати [db2\_fetch\_row()](function.db2-fetch-row.md) перед викликом **db2\_result()**, щоб встановити положення покажчика набору результатів.

### Список параметрів

`stmt`

Допустимий ресурс `stmt`

`column`

Або цілий індекс стовпця (починаючи з 0) в наборі результатів, або рядок, що відповідає імені стовпця.

### Значення, що повертаються

Повертає значення запитаного поля, якщо поле існує у наборі результатів. Повертає \*\*`null`\*\*якщо поле не існує і видає попередження.

### Приклади

**Пример #1 Пример использования**db2\_result()\*\*\*\*

У наступному прикладі показано, як виконати ітерацію по набору результатів за допомогою [db2\_fetch\_row()](function.db2-fetch-row.md) та отримати стовпці з набору результатів за допомогою **db2\_result()**

```php
<?php
$sql = 'SELECT name, breed FROM animals WHERE weight < ?';
$stmt = db2_prepare($conn, $sql);
db2_execute($stmt, array(10));
while (db2_fetch_row($stmt)) {
    $name = db2_result($stmt, 0);
    $breed = db2_result($stmt, 'BREED');
    print "$name $breed";
}
?>
```

Результат виконання наведеного прикладу:

```
cat Pook
gold fish Bubbles
budgerigar Gizmo
goat Rickety Ride
```

### Дивіться також

-   [db2\_fetch\_array()](function.db2-fetch-array.md) \- Повертає масив, індексований за положенням стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_assoc()](function.db2-fetch-assoc.md) \- Повертає масив, індексований на ім'я стовпця, що представляє рядок у наборі результатів
-   [db2\_fetch\_both()](function.db2-fetch-both.md) \- Повертає масив, індексований як на ім'я стовпця, так і за позицією, що представляє рядок у наборі результатів
-   [db2\_fetch\_object()](function.db2-fetch-object.md) \- Повертає об'єкт із властивостями, що становлять стовпці у вибраному рядку
-   [db2\_fetch\_row()](function.db2-fetch-row.md) \- Встановлює вказівник набору результатів на наступний рядок або запрошений рядок
