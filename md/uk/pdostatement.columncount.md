---
navigation:
  - pdostatement.closecursor.md: '« PDOStatement::closeCursor'
  - pdostatement.debugdumpparams.md: 'PDOStatement::debugDumpParams »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::columnCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::columnCount

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.2.0)

PDOStatement::columnCount — Повертає кількість стовпців у результуючому наборі

### Опис

```methodsynopsis
public PDOStatement::columnCount(): int
```

Используйте**PDOStatement::columnCount()**, щоб дізнатися кількість стовпців у результуючому наборі, який представляє об'єкт PDOStatement.

Якщо об'єкт PDOStatement був повернутий з методу [PDO::query()](pdo.query.md), Число стовпців можна дізнатися відразу ж.

Якщо об'єкт PDOStatement був повернутий з методу [PDO::prepare()](pdo.prepare.md)Точну кількість стовпців можна буде дізнатися тільки після запуску методу [PDOStatement::execute()](pdostatement.execute.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість стовпців у результуючому наборі запиту PDOStatement, навіть якщо він порожній. Якщо результуючого набору немає, **PDOStatement::columnCount()** повертає

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Підрахунок стовпців**

У цьому прикладі показано, як **PDOStatement::columnCount()** працює у разі наявності та відсутності результуючого набору.

```php
<?php
$dbh = new PDO('odbc:sample', 'db2inst1', 'ibmdb2');

$sth = $dbh->prepare("SELECT name, colour FROM fruit");

/* Подсчёт количества столбцов в (несуществующем) результирующем наборе */
$colcount = $sth->columnCount();
print "Перед вызовом execute(), в результирующем наборе $colcount столбцов (должно быть 0)\n";

$sth->execute();

/* Подсчёт количества столбцов в результирующем наборе */
$colcount = $sth->columnCount();
print "После вызова execute(), в результирующем наборе $colcount столбцов (должно быть 2)\n";

?>
```

Результат виконання наведеного прикладу:

```
Перед вызовом execute(), в результирующем наборе 0 столбцов (должно быть 0)
После вызова execute(), в результирующем наборе 2 столбцов (должно быть 2)
```

### Дивіться також

-   [PDO::prepare()](pdo.prepare.md) \- готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::execute()](pdostatement.execute.md) \- Запускає підготовлений запит на виконання
-   [PDOStatement::rowCount()](pdostatement.rowcount.md) \- Повертає кількість рядків, порушених останнім SQL-запитом
