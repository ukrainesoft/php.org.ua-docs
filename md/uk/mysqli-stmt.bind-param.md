---
navigation:
  - mysqli-stmt.attr-set.md: '« mysqli\_stmt::attr\_set'
  - mysqli-stmt.bind-result.md: 'mysqli\_stmt::bind\_result »'
  - index.md: PHP Manual
  - class.mysqli-stmt.md: mysqli\_stmt
title: 'mysqli\_stmt::bind\_param'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli\_stmt::bind\_param

# mysqli\_stmt\_bind\_param

(PHP 5, PHP 7, PHP 8)

mysqli\_stmt::bind\_param -- mysqli\_stmt\_bind\_param — Прив'язка змінних до параметрів запиту, що готується.

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli_stmt::bind_param(string $types, mixed &$var, mixed &...$vars): bool
```

Процедурний стиль

```methodsynopsis
mysqli_stmt_bind_param(    mysqli_stmt $statement,    string $types,    mixed &$var,    mixed &...$vars): bool
```

Прив'язує змінні до позначок параметрів у SQL-вираженні, яке було підготовлено функцією [mysqli\_prepare()](mysqli.prepare.md) або [mysqli\_stmt\_prepare()](mysqli-stmt.prepare.md)

> **Зауваження** :
> 
> Якщо розмір даних змінної перевищує максимально допустимий розмір пакета (max\_allowed\_packet), необхідно задати значення `b`параметру`types` та використовувати функцію [mysqli\_stmt\_send\_long\_data()](mysqli-stmt.send-long-data.md), яка передаватиме дані пакетами.

> **Зауваження** :
> 
> При использовании**mysqli\_stmt\_bind\_param()** спільно з [call\_user\_func\_array()](function.call-user-func-array.md) необхідно дотримуватися особливої ​​обережності. Потрібно брати до уваги, що **mysqli\_stmt\_bind\_param()** приймає як параметри лише посилання на значення, у той час як [call\_user\_func\_array()](function.call-user-func-array.md) приймає перелік параметрів, які можуть передаватися як за посиланням, так і за значенням.

### Список параметрів

`stmt`

Тільки для процедурного стилю: об'єкт [mysqli\_stmt](class.mysqli-stmt.md), який повернула функція [mysqli\_stmt\_init()](mysqli.stmt-init.md)

`types`

Рядок, що містить один або більше символів, кожен з яких задає тип значення змінної, що прив'язується:

**Символи, що задають тип**

| Символ | Опис |
| --- | --- |
| i | у відповідної змінної тип int |
| d | у відповідної змінної тип float |
| s | у відповідної змінної тип string |
| b | відповідна змінна є великим двійковим об'єктом (blob) і пересилатиметься пакетами |

`var`

`vars`

Кількість змінних та довжина рядка `types` повинні точно відповідати кількості параметрів у запиті.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Пример #1 Пример использования**mysqli\_stmt::bind\_param()\*\*\*\*

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');

$stmt = $mysqli->prepare("INSERT INTO CountryLanguage VALUES (?, ?, ?, ?)");
$stmt->bind_param('sssd', $code, $language, $official, $percent);

$code = 'DEU';
$language = 'Bavarian';
$official = "F";
$percent = 11.2;

$stmt->execute();

printf("строк добавлено: %d.\n", $stmt->affected_rows);

/* Clean up table CountryLanguage */
$mysqli->query("DELETE FROM CountryLanguage WHERE Language='Bavarian'");
printf("строк удалено: %d.\n", $mysqli->affected_rows);
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect('localhost', 'my_user', 'my_password', 'world');

$stmt = mysqli_prepare($link, "INSERT INTO CountryLanguage VALUES (?, ?, ?, ?)");
mysqli_stmt_bind_param($stmt, 'sssd', $code, $language, $official, $percent);

$code = 'DEU';
$language = 'Bavarian';
$official = "F";
$percent = 11.2;

mysqli_stmt_execute($stmt);

printf("строк добавлено: %d.\n", mysqli_stmt_affected_rows($stmt));

/* Clean up table CountryLanguage */
mysqli_query($link, "DELETE FROM CountryLanguage WHERE Language='Bavarian'");
printf("строк удалено: %d.\n", mysqli_affected_rows($link));
```

Результат виконання наведених прикладів:

```
строк добавлено: 1.
1 row deleted.
```

**Пример #2 Пример использования`...`для предоставления аргументов**

Оператор`...` може використовуватися для надання списку аргументів змінної довжини, наприклад, у конструкції `WHERE IN`

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli('localhost', 'my_user', 'my_password', 'world');

$stmt = $mysqli->prepare("SELECT Language FROM CountryLanguage WHERE CountryCode IN (?, ?)");
/* использование ... для предоставления аргументов */
$stmt->bind_param('ss', ...['DEU', 'POL']);
$stmt->execute();
$stmt->store_result();

printf("найдено строк: %d.\n", $stmt->num_rows());
```

Результат виконання наведених прикладів:

```
найдено строк: 10.
```

### Дивіться також

-   [mysqli\_stmt\_bind\_result()](mysqli-stmt.bind-result.md) \- Прив'язка змінних до підготовленого запиту для розміщення результату
-   [mysqli\_stmt\_execute()](mysqli-stmt.execute.md) \- Виконує підготовлене затвердження
-   [mysqli\_stmt\_fetch()](mysqli-stmt.fetch.md) \- пов'язує результати підготовленого виразу зі змінними
-   [mysqli\_prepare()](mysqli.prepare.md) \- готує SQL вираз до виконання
-   [mysqli\_stmt\_send\_long\_data()](mysqli-stmt.send-long-data.md) \- Відправлення даних блоками
-   [mysqli\_stmt\_errno()](mysqli-stmt.errno.md) \- Повертає код помилки виконання останнього запиту
-   [mysqli\_stmt\_error()](mysqli-stmt.error.md) \- Повертає рядок із поясненням останньої помилки під час виконання запиту
