---
navigation:
  - pdostatement.fetchall.md: '« PDOStatement::fetchAll'
  - pdostatement.fetchobject.md: 'PDOStatement::fetchObject »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::fetchColumn'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::fetchColumn

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.9.0)

PDOStatement::fetchColumn — Повертає дані одного стовпця наступного рядка результуючого набору

### Опис

```methodsynopsis
public PDOStatement::fetchColumn(int $column = 0): mixed
```

Повертає дані одного стовпця наступного рядка результуючої таблиці. Якщо в результаті запиту рядків більше немає, функція поверне **`false`**

> **Зауваження** :
> 
> Не слід використовувати **PDOStatement::fetchColumn()** для отримання логічних полів, тому що неможливо відрізнити значення **`false`** від відсутності рядків результату, що залишилися. Натомість використовуйте метод [PDOStatement::fetch()](pdostatement.fetch.md)

### Список параметрів

`column`

Номер стовпця, дані якого потрібно витягти. Нумерація починається з 0. Якщо параметр не встановлено, **PDOStatement::fetchColumn()** обере дані першого стовпця.

### Значення, що повертаються

Метод**PDOStatement::fetchColumn()** повертає значення одного стовпця наступного рядка результуючого набору або \*\*`false`\*\*якщо більше немає рядків.

**Увага**

При виклику методу **PDOStatement::fetchColumn()** для отримання даних з результуючого набору неможливо отримати значення іншого стовпця того ж рядка.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Отримання значення першого стовпця наступного рядка**

```php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

print "Получение значения первого столбца первой строки:\n";
$result = $sth->fetchColumn();
print "name = $result\n";

print "Получение значения второго столбца второй строки:\n";
$result = $sth->fetchColumn(1);
print "colour = $result\n";
?>
```

Результат виконання наведеного прикладу:

```
Получение значения первого столбца первой строки:
name = lemon
Получение значения второго столбца второй строки:
colour = red
```

### Дивіться також

-   [PDO::query()](pdo.query.md) \- готує та виконує вираз SQL без заповнювачів
-   [PDOStatement::fetch()](pdostatement.fetch.md) \- Вилучення наступного рядка з результуючого набору
-   [PDOStatement::fetchAll()](pdostatement.fetchall.md) \- Вибирає рядки, що залишилися, з набору результатів
-   [PDO::prepare()](pdo.prepare.md) \- готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::setFetchMode()](pdostatement.setfetchmode.md) \- Встановлює режим вибірки за промовчанням для об'єкта запиту
