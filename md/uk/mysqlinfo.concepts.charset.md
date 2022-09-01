---
navigation:
  - mysqlinfo.concepts.buffering.md: « Буферизовані та небуферизовані запити
  - book.mysqli.md: MySQLi »
  - index.md: PHP Manual
  - mysqlinfo.concepts.md: Основні поняття
title: Кодування символів
---
## Кодування символів

В ідеальному випадку кодування символів має встановлюватися на рівні сервера і робити це згідно з описом у розділі [» Конфігурація кодування символів](http://dev.mysql.com/doc/mysql/en/charset-configuration.md) документації MySQL сервера. В якості альтернативи кожен MySQL API пропонує метод встановлення кодування символів під час виконання.

**Застереження**

# Кодування символів та екранування символів

Кодування символів має бути чітко визначено, оскільки впливає на кожну дію, у тому числі на дії з наслідками безпеки. Наприклад, механізми екранування (такі як [mysqlirealescapestring()](mysqli.real-escape-string.md) для mysqli та [PDO::quote()](pdo.quote.md) для PDOMySQL) залежить від цих налаштувань. Важливо розуміти, що ці функції не використовують кодування символів, визначене у запиті, наприклад, такі запити не впливатимуть на поведінку цих функцій:

**Приклад #1 Проблеми встановлення кодування символів за допомогою SQL**

```php
<?php

$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

// Этот запрос не влияет на поведение $mysqli->real_escape_string();
$mysqli->query("SET NAMES utf8mb4");

// И этот не влияет на $mysqli->real_escape_string();
$mysqli->query("SET CHARACTER SET utf8mb4");

// но вот этот запрос повлияет на поведение $mysqli->real_escape_string();
$mysqli->set_charset('utf8mb4');

// а этот НЕ повлияет, потому что нельзя использовать "-"
$mysqli->set_charset('UTF-8'); // (utf8mb4, а не UTF-8)
?>
```

Приклади нижче демонструють, як правильно змінювати кодування символів під час виконання за допомогою кожного з API.

> **Зауваження** **Можлива плутанина з UTF-8**
> 
> Оскільки імена кодувань символів у MySQL не містять тире/дефіс, рядок "utf8" застосовується в MySQL для встановлення кодування UTF-8 (до 3 байт у кодуванні Unicode UTF-8). Рядок "UTF-8" неприйнятний і викине помилку під час встановлення кодування символів.

**Приклад #2 Приклад встановлення кодування символів: mysqli**

```php
<?php
$mysqli = new mysqli("localhost", "my_user", "my_password", "world");

echo 'Первоначальная кодировка: ' . $mysqli->character_set_name() . "\n";

if (!$mysqli->set_charset('utf8mb4')) {
    printf("Ошибка загрузки кодировки utf8mb4: %s\n", $mysqli->error);
    exit;
}

echo 'Ваша текущая кодировка: ' . $mysqli->character_set_name() . "\n";
?>
```

**Приклад #3 Приклад встановлення кодування символів: [pdomysql](ref.pdo-mysql.connection.md)**

```php
<?php
$pdo = new PDO("mysql:host=localhost;dbname=world;charset=utf8mb4", 'my_user', 'my_pass');
?>
```
