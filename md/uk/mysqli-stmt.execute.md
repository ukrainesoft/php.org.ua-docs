---
navigation:
  - mysqli-stmt.error.html: '« mysqlistmt::$error'
  - mysqli-stmt.fetch.html: 'mysqlistmt::fetch »'
  - index.html: PHP Manual
  - class.mysqli-stmt.html: mysqlistmt
title: 'mysqlistmt::execute'
---
# mysqlistmt::execute

# mysqlistmtexecute

(PHP 5, PHP 7, PHP 8)

mysqlistmt::execute -- mysqlistmtexecute — Виконує підготовлене затвердження

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::execute(?array $params = null): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_execute(mysqli_stmt $statement, ?array $params = null): bool
```

Виконує заздалегідь підготовлене твердження. Твердження має бути успішно підготовлене перед виконанням з використанням функції [mysqliprepare()](mysqli.prepare.html) або [mysqlistmtprepare()](mysqli-stmt.prepare.html), або шляхом передачі другого аргументу в [mysqlistmt::construct()](mysqli-stmt.construct.html)

Якщо виконуються запити `UPDATE` `DELETE`, або `INSERT`, то кількість змінених рядків можна визначити функцією [mysqlistmtaffectedrows()](mysqli-stmt.affected-rows.html). Якщо запит повертає набір результатів, його можна отримати за допомогою функції [mysqlistmtgetresult()](mysqli-stmt.get-result.html) або шляхом отримання построчно безпосередньо з оператора за допомогою функції [mysqlistmtfetch()](mysqli-stmt.fetch.html)

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

`params`

Необов'язковий масив елементів (array) з кількістю елементів дорівнює кількості пов'язаних параметрів у SQL-запиті. Кожне значення сприймається як рядок (string).

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | Додано необов'язковий параметр `params` |

### Приклади

**Приклад #1 Виконання підготовленого оператора із прив'язкою змінних**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

$mysqli->query("CREATE TEMPORARY TABLE myCity LIKE City");

/* Подготавливаем утверждение на вставку строк */
$stmt = $mysqli->prepare("INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)");

/* Связываем переменные с метками */
$stmt->bind_param("sss", $val1, $val2, $val3);

$val1 = 'Stuttgart';
$val2 = 'DEU';
$val3 = 'Baden-Wuerttemberg';

/* Выполняем утверждение */
$stmt->execute();

$val1 = 'Bordeaux';
$val2 = 'FRA';
$val3 = 'Aquitaine';

/* Выполняем утверждение */
$stmt->execute();

/* Получаем все строки из myCity */
$query = "SELECT Name, CountryCode, District FROM myCity";
$result = $mysqli->query($query);
while ($row = $result->fetch_row()) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect("localhost", "my_user", "my_password", "world");

mysqli_query($link, "CREATE TEMPORARY TABLE myCity LIKE City");

/* Подготавливаем утверждение на вставку строк */
$stmt = mysqli_prepare($link, "INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)");

/* Связываем переменные с метками */
mysqli_stmt_bind_param($stmt, "sss", $val1, $val2, $val3);

$val1 = 'Stuttgart';
$val2 = 'DEU';
$val3 = 'Baden-Wuerttemberg';

/* Выполняем утверждение */
mysqli_stmt_execute($stmt);

$val1 = 'Bordeaux';
$val2 = 'FRA';
$val3 = 'Aquitaine';

/* Выполняем утверждение */
mysqli_stmt_execute($stmt);

/* Получаем все строки из myCity */
$query = "SELECT Name, CountryCode, District FROM myCity";
$result = mysqli_query($link, $query);
while ($row = mysqli_fetch_row($result)) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Результат виконання даних прикладів:

```
Stuttgart (DEU,Baden-Wuerttemberg)
Bordeaux (FRA,Aquitaine)
```

**Приклад #2 Виконання підготовленого оператора з масивом значень**

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');

$mysqli->query('CREATE TEMPORARY TABLE myCity LIKE City');

/* Подготавливаем утверждение на вставку строк */
$stmt = $mysqli->prepare('INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)');

/* Выполняем утверждение */
$stmt->execute(['Stuttgart', 'DEU', 'Baden-Wuerttemberg']);

/* Получаем все строки из myCity */
$query = 'SELECT Name, CountryCode, District FROM myCity';
$result = $mysqli->query($query);
while ($row = $result->fetch_row()) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect('localhost', 'my_user', 'my_password', 'world');

mysqli_query($link, 'CREATE TEMPORARY TABLE myCity LIKE City');

/* Подготавливаем утверждение на вставку строк */
$stmt = mysqli_prepare($link, 'INSERT INTO myCity (Name, CountryCode, District) VALUES (?,?,?)');

/* Выполняем утверждение */
mysqli_stmt_execute($stmt, ['Stuttgart', 'DEU', 'Baden-Wuerttemberg']);

/* Получаем все строки из myCity */
$query = 'SELECT Name, CountryCode, District FROM myCity';
$result = mysqli_query($link, $query);
while ($row = mysqli_fetch_row($result)) {
    printf("%s (%s,%s)\n", $row[0], $row[1], $row[2]);
}
```

Результат виконання даних прикладів:

```
Stuttgart (DEU,Baden-Wuerttemberg)
```

### Дивіться також

-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqlistmtbindparam()](mysqli-stmt.bind-param.html) - Прив'язка змінних до параметрів запиту, що готується.
-   [mysqlistmtgetresult()](mysqli-stmt.get-result.html) - Отримує результат із підготовленого запиту у вигляді об'єкта mysqliresult
