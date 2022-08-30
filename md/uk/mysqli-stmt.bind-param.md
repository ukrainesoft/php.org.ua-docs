Прив'язка змінних до параметрів запиту, що готується.

-   [« mysqlistmt::attrset](mysqli-stmt.attr-set.html)
    
-   [mysqlistmt::bindresult »](mysqli-stmt.bind-result.html)
    
-   [PHP Manual](index.html)
    
-   [mysqlistmt](class.mysqli-stmt.html)
    
-   Прив'язка змінних до параметрів запиту, що готується.
    

# mysqlistmt::bindparam

# mysqlistmtbindparam

(PHP 5, PHP 7, PHP 8)

mysqlistmt::bindparam - mysqlistmtbindparam — Прив'язка змінних до параметрів запиту, що готується.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::bind_param(string $types, mixed &$var, mixed &...$vars): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_bind_param(    mysqli_stmt $statement,    string $types,    mixed &$var,    mixed &...$vars): bool
```

Прив'язує змінні до міток параметрів у SQL-вираженні, яке було підготовлене функцією [mysqliprepare()](mysqli.prepare.html) або [mysqlistmtprepare()](mysqli-stmt.prepare.html)

> **Зауваження**
> 
> Якщо розмір даних змінної перевищує максимально допустимий розмір пакета (maxallowedpacket), необхідно задати значення `b` параметром `types` та використовувати функцію [mysqlistmtsendlongdata()](mysqli-stmt.send-long-data.html), яка передаватиме дані пакетами.

> **Зауваження**
> 
> При використанні **mysqlistmtbindparam()** спільно з [calluserfuncarray()](function.call-user-func-array.html) необхідно дотримуватися особливої ​​обережності. Потрібно брати до уваги, що **mysqlistmtbindparam()** приймає як параметри лише посилання на значення, у той час як [calluserfuncarray()](function.call-user-func-array.html) приймає перелік параметрів, які можуть передаватися як за посиланням, так і за значенням.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqlistmt](class.mysqli-stmt.html), отриманий за допомогою [mysqlistmtinit()](mysqli.stmt-init.html)

`types`

Рядок, що містить один або більше символів, кожен з яких задає тип значення змінної, що прив'язується:

**Символи, що задають тип**

| Символ | Описание                                                                          |
|--------|-----------------------------------------------------------------------------------|
| і      | відповідна змінна має тип integer                                                 |
| д      | відповідна змінна має тип double                                                  |
| з      | відповідна змінна має тип string                                                  |
| в      | відповідна змінна є великим двійковим об'єктом (blob) і пересилатиметься пакетами |

`var`

`vars`

Кількість змінних та довжина рядка `types` повинні точно відповідати кількості параметрів у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqlistmt::bindparam()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');

$stmt = $mysqli->prepare("INSERT INTO CountryLanguage VALUES (?, ?, ?, ?)");
$stmt->bind_param('sssd', $code, $language, $official, $percent);

$code = 'DEU';
$language = 'Bavarian';
$official = "F";
$percent = 11.2;

$stmt->execute();

printf("строк добавлено: %d.\n", $stmt->affected_rows);

/* Clean up table CountryLanguage */
$mysqli->query("DELETE FROM CountryLanguage WHERE Language='Bavarian'");
printf("строк удалено: %d.\n", $mysqli->affected_rows);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect('localhost', 'my_user', 'my_password', 'world');

$stmt = mysqli_prepare($link, "INSERT INTO CountryLanguage VALUES (?, ?, ?, ?)");
mysqli_stmt_bind_param($stmt, 'sssd', $code, $language, $official, $percent);

$code = 'DEU';
$language = 'Bavarian';
$official = "F";
$percent = 11.2;

mysqli_stmt_execute($stmt);

printf("строк добавлено: %d.\n", mysqli_stmt_affected_rows($stmt));

/* Clean up table CountryLanguage */
mysqli_query($link, "DELETE FROM CountryLanguage WHERE Language='Bavarian'");
printf("строк удалено: %d.\n", mysqli_affected_rows($link));
```

Результат виконання даних прикладів:

```
строк добавлено: 1.
1 row deleted.
```

**Приклад #2 Приклад використання `...` для надання аргументів**

Оператор `...` може використовуватися для надання списку аргументів змінної довжини, наприклад, у конструкції `WHERE IN`

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');

$stmt = $mysqli->prepare("SELECT Language FROM CountryLanguage WHERE CountryCode IN (?, ?)");
/* использование ... для предоставления аргументов */
$stmt->bind_param('ss', ...['DEU', 'POL']);
$stmt->execute();
$stmt->store_result();

printf("найдено строк: %d.\n", $stmt->num_rows());
```

Результат виконання даних прикладів:

```
найдено строк: 10.
```

### Дивіться також

-   [mysqlistmtbindresult()](mysqli-stmt.bind-result.html) - Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqlistmtexecute()](mysqli-stmt.execute.html) - Виконує підготовлене затвердження
-   [mysqlistmtfetch()](mysqli-stmt.fetch.html) - пов'язує результати підготовленого виразу зі змінними
-   [mysqliprepare()](mysqli.prepare.html) - готує SQL вираз до виконання
-   [mysqlistmtsendlongdata()](mysqli-stmt.send-long-data.html) - Відправлення даних блоками
-   [mysqlistmterrno()](mysqli-stmt.errno.html) - Повертає код помилки виконання останнього запиту
-   [mysqlistmterror()](mysqli-stmt.error.html) - Повертає рядок із поясненням останньої помилки під час виконання запиту