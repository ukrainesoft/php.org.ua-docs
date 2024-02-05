---
navigation:
  - mysqli.select-db.md: '« mysqli::select\_db'
  - mysqli.sqlstate.md: 'mysqli::$sqlstate »'
  - index.md: PHP Manual
  - class.mysqli.md: mysqli
title: 'mysqli::set\_charset'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# mysqli::set\_charset

# mysqli\_set\_charset

(PHP 5 >= 5.0.5, PHP 7, PHP 8)

mysqli::set\_charset -- mysqli\_set\_charset — Встановлює набір символів

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

Тільки для процедурного стилю: об'єкт [mysqli](class.mysqli.md), який повернула функція [mysqli\_connect()](function.mysqli-connect.md)или функция[mysqli\_init()](mysqli.init.md)

`charset`

Набір символів, які потрібно встановити.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Якщо сповіщення про помилки mysqli включено (**`MYSQLI_REPORT_ERROR`**) та запитана операція не вдалася, видається попередження. Якщо, крім того, встановлено режим **`MYSQLI_REPORT_STRICT`**, натомість буде викинуто виняток [mysqli\_sql\_exception](class.mysqli-sql-exception.md)

### Приклади

**Пример #1 Пример использования**mysqli::set\_charset()\*\*\*\*

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

Результат виконання наведених прикладів:

```
Начальный набор символов: latin1
Текущий набор символов: utf8mb4
```

### Примітки

> **Зауваження** :
> 
> Щоб використовувати цю функцію на Windows платформах, вам знадобиться клієнтська бібліотека MySQL версії 4.1.11 або вище (для MySQL 5.0 відповідно 5.0.6 або вище).

> **Зауваження** :
> 
> Це найкращий спосіб завдання набору символів. Використання з цією метою функції [mysqli\_query()](mysqli.query.md)(например`SET NAMES utf8`) не рекомендуется. Дополнительно смотрите[Набори символів у MySQL](mysqlinfo.concepts.charset.md)

### Дивіться також

-   [mysqli\_character\_set\_name()](mysqli.character-set-name.md) \- Повертає поточне кодування, встановлене для з'єднання з БД
-   [mysqli\_real\_escape\_string()](mysqli.real-escape-string.md) \- Екранує спеціальні символи у рядку для використання у SQL-вираженні, використовуючи поточний набір символів з'єднання
-   [Концепції кодувань MySQL](mysqlinfo.concepts.charset.md)
-   [» Список підтримуваних MySQL наборів символів](http://dev.mysql.com/doc/mysql/en/charset-charsets.md)
