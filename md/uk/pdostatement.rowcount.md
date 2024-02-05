---
navigation:
  - pdostatement.nextrowset.md: '« PDOStatement::nextRowset'
  - pdostatement.setattribute.md: 'PDOStatement::setAttribute »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::rowCount'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::rowCount

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

PDOStatement::rowCount — Повертає кількість рядків, порушених останнім SQL-запитом

### Опис

```methodsynopsis
public PDOStatement::rowCount(): int
```

**PDOStatement::rowCount()** повертає кількість рядків, які торкнулися під час виконання останнього запиту DELETE, INSERT чи UPDATE, запущеного відповідним об'єктом `PDOStatement`

Для операторів, які створюють набори результатів, таких як `SELECT`, поведінка не визначена і може бути різною для кожного драйвера. Деякі бази даних можуть повертати кількість рядків, створених цим оператором (наприклад, MySQL у буферизованому режимі), але така поведінка не гарантується для всіх баз даних і не повинна використовуватися в програмах, що переносяться.

> **Зауваження** :
> 
> Цей метод завжди повертає "0" (нуль) з драйвером SQLite, а з драйвером PostgreSQL лише при встановленні атрибута оператора **`PDO::ATTR_CURSOR`** рівним **`PDO::CURSOR_SCROLL`**

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає кількість рядків.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Отримання кількості віддалених рядків**

**PDOStatement::rowCount()** повертає кількість рядків, змінених виразами DELETE, INSERT чи UPDATE.

```php
<?php
/* Удалим все строки из таблицы FRUIT */
$del = $dbh->prepare('DELETE FROM fruit');
$del->execute();

/* Выведем число удалённых строк */
print "Количество удалённых строк:\n";
$count = $del->rowCount();
print "Удалено $count строк.\n";
?>
```

Висновок наведеного прикладу буде схожим на:

```
Количество удалённых строк:
Удалено 9 строк.
```

**Приклад #2 Підрахунок рядків, що повертаються виразом SELECT**

Для большинства СУБД**PDOStatement::rowCount()** не повертає кількість рядків, які торкнулися SELECT запитом. Замість цього методу запустіть через [PDO::query()](pdo.query.md) вираз SELECT COUNT(\*) з тим самим текстом запиту. Потім методом [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) ви отримаєте число рядків, що збігаються.

```php
<?php
$sql = "SELECT COUNT(*) FROM fruit WHERE calories > 100";
$res = $conn->query($sql);
$count = $res->fetchColumn();

print "Совпадающих записей: " .  $count;
?>
```

Висновок наведеного прикладу буде схожим на:

```
Совпадающих записей: 2
```

### Дивіться також

-   [PDOStatement::columnCount()](pdostatement.columncount.md) \- Повертає кількість стовпців у результуючому наборі
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) \- Повертає дані одного стовпця наступного рядка результуючого набору
-   [PDO::query()](pdo.query.md) \- готує та виконує вираз SQL без заповнювачів
