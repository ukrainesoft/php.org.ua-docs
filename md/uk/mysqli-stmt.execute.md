---
navigation:
  - mysqli-stmt.error.md: '« mysqli\_stmt::$error'
  - mysqli-stmt.fetch.md: 'mysqli\_stmt::fetch »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::execute

# mysqli\_stmt\_execute

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::execute -- mysqli\_stmt\_execute — Виконує підготовлене затвердження

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::execute(?array $params = null): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_execute(mysqli_stmt $statement, ?array $params = null): bool
```

Виконує заздалегідь підготовлене твердження. Твердження має бути успішно підготовлене перед виконанням з використанням функції [mysqli\_prepare()](mysqli.prepare.md) або [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.md), або шляхом передачі другого аргументу в [mysqli\_stmt::\_\_construct()](mysqli-stmt.construct.md)

Якщо виконуються запити `UPDATE` `DELETE`, или`INSERT`, то кількість змінених рядків можна визначити функцією [mysqli\_stmt\_affected\_rows()](mysqli-stmt.affected-rows.md). Якщо запит повертає набір результатів, його можна отримати за допомогою функції [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md) або шляхом отримання построчно безпосередньо з оператора за допомогою функції [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`params`

Необов'язковий масив елементів (array) з кількістю елементів дорівнює кількості пов'язаних параметрів у SQL-запиті. Кожне значення сприймається як рядок (string).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### список змін

| Версия | Опис |
| --- | --- |
| 8.1.0 | Додано необов'язковий параметр `params` |

### Приклади

**Приклад #1 Виконання підготовленого оператора із прив'язкою змінних**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$mysqli->query("CREATE TEMPORARY TABLE myCity LIKE City");

/* Подготавливаем утверждение на вставку строк */
$stmt = $mysqli->prepare("INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)");

/* Связываем переменные с метками */
$stmt->bind_param("sss", $val1, $val2, $val3);

$val1 = 'Stuttgart';
$val2 = 'DEU';
$val3 = 'Baden-Wuerttemberg';

/* Выполняем утверждение */
$stmt->execute();

$val1 = 'Bordeaux';
$val2 = 'FRA';
$val3 = 'Aquitaine';

/* Выполняем утверждение */
$stmt->execute();

/* Получаем все строки из myCity */
$query = "SELECT Name, CountryCode, District FROM myCity";
$result = $mysqli->query($query);
while ($row = $result->fetch_row()) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

mysqli_query($link, "CREATE TEMPORARY TABLE myCity LIKE City");

/* Подготавливаем утверждение на вставку строк */
$stmt = mysqli_prepare($link, "INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)");

/* Связываем переменные с метками */
mysqli_stmt_bind_param($stmt, "sss", $val1, $val2, $val3);

$val1 = 'Stuttgart';
$val2 = 'DEU';
$val3 = 'Baden-Wuerttemberg';

/* Выполняем утверждение */
mysqli_stmt_execute($stmt);

$val1 = 'Bordeaux';
$val2 = 'FRA';
$val3 = 'Aquitaine';

/* Выполняем утверждение */
mysqli_stmt_execute($stmt);

/* Получаем все строки из myCity */
$query = "SELECT Name, CountryCode, District FROM myCity";
$result = mysqli_query($link, $query);
while ($row = mysqli_fetch_row($result)) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Результат виконання наведених прикладів:

```
Stuttgart (DEU,Baden-Wuerttemberg)
Bordeaux (FRA,Aquitaine)
```

**Приклад #2 Виконання підготовленого оператора з масивом значень**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');

$mysqli->query('CREATE TEMPORARY TABLE myCity LIKE City');

/* Подготавливаем утверждение на вставку строк */
$stmt = $mysqli->prepare('INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)');

/* Выполняем утверждение */
$stmt->execute(['Stuttgart', 'DEU', 'Baden-Wuerttemberg']);

/* Получаем все строки из myCity */
$query = 'SELECT Name, CountryCode, District FROM myCity';
$result = $mysqli->query($query);
while ($row = $result->fetch_row()) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect('localhost', 'my_user', 'my_password', 'world');

mysqli_query($link, 'CREATE TEMPORARY TABLE myCity LIKE City');

/* Подготавливаем утверждение на вставку строк */
$stmt = mysqli_prepare($link, 'INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)');

/* Выполняем утверждение */
mysqli_stmt_execute($stmt, ['Stuttgart', 'DEU', 'Baden-Wuerttemberg']);

/* Получаем все строки из myCity */
$query = 'SELECT Name, CountryCode, District FROM myCity';
$result = mysqli_query($link, $query);
while ($row = mysqli_fetch_row($result)) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Результат виконання наведених прикладів:

```
Stuttgart (DEU,Baden-Wuerttemberg)
```

### Дивіться також

-   [mysqli\_execute\_query()](mysqli.execute-query.md) \- готує, зв'язує параметри та виконує SQL-запит
-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_bind\_param()](mysqli-stmt.bind-param.md) \- Прив'язка змінних до параметрів запиту, що готується.
-   [mysqli\_stmt\_get\_result()](mysqli-stmt.get-result.md) \- Отримує результат із підготовленого запиту у вигляді об'єкта mysqli\_result
