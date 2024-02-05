---
navigation:
  - pdostatement.columncount.md: '« PDOStatement::columnCount'
  - pdostatement.errorcode.md: 'PDOStatement::errorCode »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::debugDumpParams'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::debugDumpParams

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.9.0)

PDOStatement::debugDumpParams — Виведення інформації про підготовлену SQL-команду з метою налагодження

### Опис

```methodsynopsis
public PDOStatement::debugDumpParams(): ?bool
```

Виводить інформацію про підготовлений запит у вихідний потік. Виводитиметься текст використовуваного `SQL` запиту, кількість задіяних параметрів (`Params`), список параметрів з їх іменами ключів або індексами, їх іменами, індексами у запиті (якщо підтримується в драйвері PDO, інакше -1), типом (`param_type`) у вигляді цілого числа та логічне значення `is_param`

Це функція налагодження, яка направляє дані на стандартний висновок.

**Підказка**

Як і все, що виводить результат у браузер, [функції контролю виведення](book.outcontrol.md) можна викликати, щоб перехопити дані, що виводяться цією функцією, і зберігати їх, наприклад у рядок (string).

Ця функція виводить інформацію про параметри запиту, які існують на момент дзвінка. Додаткові параметри не зберігаються у запиті, тому не відображаються.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає \*\*`null`**или**`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 7.2.0 | **PDOStatement::debugDumpParams()** тепер повертає SQL, відправлений до бази даних, зокрема повний необроблений запит (включаючи замінені параметри зі своїми пов'язаними значеннями). Зверніть увагу, що це буде працювати тільки при включеній емуляції запитів, що готуються. |

### Приклади

**Пример #1 Пример использования**PDOStatement::debugDumpParams()\*\* з іменованими параметрами\*\*

```php
<?php
/* Выполнение запроса с привязкой PHP переменных */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->bindParam(':calories', $calories, PDO::PARAM_INT);
$sth->bindValue(':colour', $colour, PDO::PARAM_STR, 12);
$sth->execute();

$sth->debugDumpParams();

?>
```

Результат виконання наведеного прикладу:

```
SQL: [96] SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour
Params:  2
Key: Name: [9] :calories
paramno=-1
name=[9] ":calories"
is_param=1
param_type=1
Key: Name: [7] :colour
paramno=-1
name=[7] ":colour"
is_param=1
param_type=2
```

**Пример #2 Пример использования**PDOStatement::debugDumpParams()\*\* з неіменованими (?) параметрами\*\*

```php
<?php

/* Выполнение запроса с привязкой PHP переменных */
$calories = 150;
$colour = 'red';
$name = 'apple';

$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindParam(1, $calories, PDO::PARAM_INT);
$sth->bindValue(2, $colour, PDO::PARAM_STR);
$sth->execute();

$sth->debugDumpParams();

?>
```

Результат виконання наведеного прикладу:

```
SQL: [82] SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?
Params:  2
Key: Position #0:
paramno=0
name=[0] ""
is_param=1
param_type=1
Key: Position #1:
paramno=1
name=[0] ""
is_param=1
param_type=2
```

### Дивіться також

-   [PDO::prepare()](pdo.prepare.md) \- готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::bindParam()](pdostatement.bindparam.md) \- Прив'язує параметр запиту до змінної
-   [PDOStatement::bindValue()](pdostatement.bindvalue.md) \- Зв'язує параметр із заданим значенням
