Повертає кількість стовпців у результуючому наборі

-   [« PDOStatement::closeCursor](pdostatement.closecursor.html)
    
-   [PDOStatement::debugDumpParams »](pdostatement.debugdumpparams.html)
    
-   [PHP Manual](index.html)
    
-   [PDOStatement](class.pdostatement.html)
    
-   Повертає кількість стовпців у результуючому наборі
    

# PDOStatement::columnCount

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.2.0)

PDOStatement::columnCount — Повертає кількість стовпців у результуючому наборі

### Опис

```methodsynopsis
public PDOStatement::columnCount(): int
```

Використовуйте **PDOStatement::columnCount()**, щоб дізнатися кількість стовпців у результуючому наборі, який представляє об'єкт PDOStatement.

Якщо об'єкт PDOStatement був повернутий з методу [PDO::query()](pdo.query.html), Число стовпців можна дізнатися відразу ж.

Якщо об'єкт PDOStatement був повернутий з методу [PDO::prepare()](pdo.prepare.html)Точну кількість стовпців можна буде дізнатися тільки після запуску методу [PDOStatement::execute()](pdostatement.execute.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість стовпців у результуючому наборі запиту PDOStatement, навіть якщо він порожній. Якщо результуючого набору немає, **PDOStatement::columnCount()** повертає `0`

### Приклади

**Приклад #1 Підрахунок стовпців**

У цьому прикладі показано, як **PDOStatement::columnCount()** працює у разі наявності та відсутності результуючого набору.

```php
<?php
$dbh = new PDO('odbc:sample', 'db2inst1', 'ibmdb2');

$sth = $dbh->prepare("SELECT name, colour FROM fruit");

/* Подсчёт количества столбцов в (несуществующем) результирующем наборе */
$colcount = $sth->columnCount();
print("Перед вызовом execute(), в результирующем наборе $colcount столбцов (должно быть 0)\n");

$sth->execute();

/* Подсчёт количества столбцов в результирующем наборе */
$colcount = $sth->columnCount();
print("После вызова execute(), в результирующем наборе $colcount столбцов (должно быть 2)\n");

?>
```

Результат виконання цього прикладу:

```
Перед вызовом execute(), в результирующем наборе 0 столбцов (должно быть 0)
После вызова execute(), в результирующем наборе 2 столбцов (должно быть 2)
```

### Дивіться також

-   [PDO::prepare()](pdo.prepare.html) - готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::execute()](pdostatement.execute.html) - Запускає підготовлений запит на виконання
-   [PDOStatement::rowCount()](pdostatement.rowcount.html) - Повертає кількість рядків, порушених останнім SQL-запитом