---
navigation:
  - mysqli.select-db.md: '« mysqli::selectдб'
  - mysqli.sqlstate.md: 'mysqli::$sqlstate »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::setcharset'
---
# mysqli::setcharset

# mysqlisetcharset

(PHP 5> = 5.0.5, PHP 7, PHP 8)

mysqli::setcharset - mysqlisetcharset — Встановлює набір символів

### Опис

Об'єктно-орієнтований стиль

```methodsynopsis
public mysqli::set_charset(string $charset): bool
```

Процедурний стиль

```methodsynopsis
mysqli_set_charset(mysqli $mysql, string $charset): bool
```

Задає набір символів, який буде використовуватися для обміну даними з сервером баз даних.

### Список параметрів

`mysql`

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), отриманий за допомогою [mysqliconnect()](function.mysqli-connect.md) або [mysqliinit()](mysqli.init.md)

`charset`

Набір символів, які потрібно встановити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **mysqli::setcharset()****

Об'єктно-орієнтований стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$mysqli = new mysqli("localhost", "my_user", "my_password", "test");

printf("Начальный набор символов: %s\n", $mysqli->character_set_name());

/* изменение набора символов на utf8mb4 */
$mysqli->set_charset("utf8mb4");

printf("Текущий набор символов: %s\n", $mysqli->character_set_name());
```

Процедурний стиль

```php
<?php

mysqli_report(MYSQLI_REPORT_ERROR | MYSQLI_REPORT_STRICT);
$link = mysqli_connect('localhost', 'my_user', 'my_password', 'test');

printf("Начальный набор символов: %s\n", mysqli_character_set_name($link));

/* изменение набора символов на utf8mb4 */
mysqli_set_charset($link, "utf8mb4");

printf("Текущий набор символов: %s\n", mysqli_character_set_name($link));
```

Результат виконання даних прикладів:

```
Начальный набор символов: latin1
Текущий набор символов: utf8mb4
```

### Примітки

> **Зауваження**
> 
> Щоб використовувати цю функцію на Windows платформах, вам знадобиться клієнтська бібліотека MySQL версії 4.1.11 або вище (для MySQL 5.0 відповідно 5.0.6 або вище).

> **Зауваження**
> 
> Це найкращий спосіб завдання набору символів. Використання з цією метою функції [mysqliquery()](mysqli.query.md) (наприклад `SET NAMES utf8`) не рекомендується. Додатково дивіться [Набори символів у MySQL](mysqlinfo.concepts.charset.md)

### Дивіться також

-   [mysqlicharactersetname()](mysqli.character-set-name.md) - Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqlirealescapestring()](mysqli.real-escape-string.md) - Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання
-   [Концепції кодувань MySQL](mysqlinfo.concepts.charset.md)
-   [» Список підтримуваних MySQL наборів символів](http://dev.mysql.com/doc/mysql/en/charset-charsets.md)
