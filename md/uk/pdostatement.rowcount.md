---
navigation:
  - pdostatement.nextrowset.md: '« PDOStatement::nextRowset'
  - pdostatement.setattribute.md: 'PDOStatement::setAttribute »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::rowCount'
---
# PDOStatement::rowCount

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.1.0)

PDOStatement::rowCount — Повертає кількість рядків, порушених останнім SQL-запитом

### Опис

```methodsynopsis
public PDOStatement::rowCount(): int
```

**PDOStatement::rowCount()** повертає кількість рядків, які торкнулися під час виконання останнього запиту DELETE, INSERT чи UPDATE, запущеного відповідним об'єктом `PDOStatement`

Якщо останнім запитом, запущеним відповідним об'єктом `PDOStatement`, було SQL-вираз SELECT, деякі СУБД можуть повернути кількість рядків у результуючому наборі. Однак, така поведінка методу не гарантується для всіх баз даних, і це потрібно враховувати під час проектування програм.

> **Зауваження**
> 
> Цей метод завжди повертає "0" (нуль) з драйвером SQLite, а з драйвером PostgreSQL лише при встановленні атрибута оператора **`PDO::ATTR_CURSOR`** рівним **`PDO::CURSOR_SCROLL`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість рядків.

### Приклади

**Приклад #1 Отримання кількості віддалених рядків**

**PDOStatement::rowCount()** повертає кількість рядків, змінених виразами DELETE, INSERT чи UPDATE.

```php
<?php
/* Удалим все строки из таблицы FRUIT */
$del = $dbh->prepare('DELETE FROM fruit');
$del->execute();

/* Выведем число удалённых строк */
print("Количество удалённых строк:\n");
$count = $del->rowCount();
print("Удалено $count строк.\n");
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Количество удалённых строк:
Удалено 9 строк.
```

**Приклад #2 Підрахунок рядків, що повертаються виразом SELECT**

Для більшості СУБД **PDOStatement::rowCount()** не повертає кількість рядків, які торкнулися SELECT запитом. Замість цього методу запустіть через [PDO::query()](pdo.query.md) вираз SELECT COUNT() з тим самим текстом запиту. Потім методом [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) ви отримаєте число рядків, що збігаються.

```php
<?php
$sql = "SELECT COUNT(*) FROM fruit WHERE calories > 100";
$res = $conn->query($sql);
$count = $res->fetchColumn();

print "Совпадающих записей: " .  $count;
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Совпадающих записей: 2
```

### Дивіться також

-   [PDOStatement::columnCount()](pdostatement.columncount.md) - Повертає кількість стовпців у результуючому наборі
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) - Повертає дані одного стовпця наступного рядка результуючого набору
-   [PDO::query()](pdo.query.md) - готує та виконує вираз SQL без заповнювачів
