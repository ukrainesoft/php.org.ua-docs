---
navigation:
  - mysqli.init.md: '« mysqli::init'
  - mysqli.kill.md: 'mysqli::kill »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::$insert\_id'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::$insert\_id

# mysqli\_insert\_id

(PHP 5, PHP 7, PHP 8)

mysqli::$insert\_id -- mysqli\_insert\_id — Повертає значення, створене для стовпця AUTO\_INCREMENT останнім запитом

### Опис

Об'єктно-орієнтований стиль

int|string[$mysqli->insert\_id](mysqli.insert-id.md)

Процедурний стиль

```methodsynopsis
mysqli_insert_id(mysqli $mysql): int|string
```

Повертає ідентифікатор, згенерований запитом `INSERT`или`UPDATE` для таблиці зі стовпцем, що має атрибут `AUTO_INCREMENT`. У разі багаторядкового оператора `INSERT` він повертає перше автоматично згенероване значення, яке було успішно додано.

Виконання запиту `INSERT`или`UPDATE`с использованием MySQL-функции`LAST_INSERT_ID()`также изменит значение, возвращаемое**mysqli\_insert\_id()**. Якщо `LAST_INSERT_ID(expr)` використовувався для генерації значення `AUTO_INCREMENT`, він повертає значення останнього `expr` замість згенерованого значення `AUTO_INCREMENT`

Повертає , якщо попередній оператор не змінив значення `AUTO_INCREMENT`. . **mysqli\_insert\_id()** повинен викликатись відразу після запиту, що згенерував значення.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

### Значення, що повертаються

Значение поля`AUTO_INCREMENT`, яке торкнулося попереднім запитом. Повертає нуль, якщо попередній запит не торкнувся таблиці, що містять поле `AUTO_INCREMENT`

Тільки запити, видані з використанням поточного з'єднання, впливають на значення, що повертається. На значення не впливають запити, видані за допомогою інших підключень або клієнтів.

> **Зауваження** :
> 
> Якщо число більше за максимальне значення цілого числа, функція поверне рядок.

### Приклади

**Приклад #1 Приклад функції $mysqli->insert\_id**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$mysqli->query("CREATE TABLE myCity LIKE City");

$query = "INSERT INTO myCity VALUES (NULL, 'Stuttgart', 'DEU', 'Stuttgart', 617000)";
$mysqli->query($query);

printf("ID новой записи: %d.\n", $mysqli->insert_id);

/* удаление таблицы */
$mysqli->query("DROP TABLE myCity");
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

mysqli_query($link, "CREATE TABLE myCity LIKE City");

$query = "INSERT INTO myCity VALUES (NULL, 'Stuttgart', 'DEU', 'Stuttgart', 617000)";
mysqli_query($link, $query);

printf("ID новой записи: %d.\n", mysqli_insert_id($link));

/* удаление таблицы */
mysqli_query($link, "DROP TABLE myCity");
```

Результат виконання наведених прикладів:

```
ID новой записи: 1.
```
