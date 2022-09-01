---
navigation:
  - pdostatement.fetchcolumn.html: '« PDOStatement::fetchColumn'
  - pdostatement.getattribute.html: 'PDOStatement::getAttribute »'
  - index.html: PHP Manual
  - class.pdostatement.html: PDOStatement
title: 'PDOStatement::fetchObject'
---
# PDOStatement::fetchObject

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.2.4)

PDOStatement::fetchObject — Витягує наступний рядок і повертає його як об'єкт

### Опис

```methodsynopsis
public PDOStatement::fetchObject(?string $class = "stdClass", array $constructorArgs = []): object|false
```

Витягує наступний рядок і повертає його у вигляді об'єкта. Цей метод є альтернативою виклику [PDOStatement::fetch()](pdostatement.fetch.html) з параметром **`PDO::FETCH_CLASS`** або **`PDO::FETCH_OBJ`**

Коли об'єкт вилучено, його властивості наповнюються значеннями відповідних стовпців, і після цього викликається його конструктор.

### Список параметрів

`class`

Ім'я класу об'єкта, що створюється.

`constructorArgs`

Елементи цього масиву будуть передані конструктор класу.

### Значення, що повертаються

Повертає новий об'єкт зазначеного класу, імена властивостей якого відповідають іменам стовпців результуючого набору або **`false`** у разі виникнення помилки.

### Дивіться також

-   [PDOStatement::fetch()](pdostatement.fetch.html) - Вилучення наступного рядка з результуючого набору
