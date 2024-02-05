---
navigation:
  - pdostatement.fetchcolumn.md: '« PDOStatement::fetchColumn'
  - pdostatement.getattribute.md: 'PDOStatement::getAttribute »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::fetchObject'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::fetchObject

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.2.4)

PDOStatement::fetchObject — Витягує наступний рядок і повертає його як об'єкт

### Опис

```methodsynopsis
public PDOStatement::fetchObject(?string $class = "stdClass", array $constructorArgs = []): object|false
```

Витягує наступний рядок і повертає його у вигляді об'єкта. Цей метод є альтернативою виклику [PDOStatement::fetch()](pdostatement.fetch.md)с параметром\*\*`PDO::FETCH_CLASS`** або **`PDO::FETCH_OBJ`\*\*

Коли об'єкт вилучено, його властивості наповнюються значеннями відповідних стовпців, і після цього викликається його конструктор.

### Список параметрів

`class`

Ім'я класу об'єкта, що створюється.

`constructorArgs`

Елементи цього масиву будуть передані конструктор класу.

### Значення, що повертаються

Повертає новий об'єкт зазначеного класу, імена властивостей якого відповідають іменам стовпців результуючого набору або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Дивіться також

-   [PDOStatement::fetch()](pdostatement.fetch.md) \- Вилучення наступного рядка з результуючого набору
