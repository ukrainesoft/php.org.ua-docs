Повертає дані одного стовпця наступного рядка результуючого набору

-   [« PDOStatement::fetchAll](pdostatement.fetchall.html)
    
-   [PDOStatement::fetchObject »](pdostatement.fetchobject.html)
    
-   [PHP Manual](index.html)
    
-   [PDOStatement](class.pdostatement.html)
    
-   Повертає дані одного стовпця наступного рядка результуючого набору
    

# PDOStatement::fetchColumn

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.9.0)

PDOStatement::fetchColumn — Повертає дані одного стовпця наступного рядка результуючого набору

### Опис

```methodsynopsis
public PDOStatement::fetchColumn(int $column = 0): mixed
```

Повертає дані одного стовпця наступного рядка результуючої таблиці. Якщо в результаті запиту рядків більше немає, функція поверне **`false`**

> **Зауваження**
> 
> Не слід використовувати **PDOStatement::fetchColumn()** для отримання булевих полів, тому що неможливо відрізнити значення **`false`** від відсутності рядків результату, що залишилися. Натомість використовуйте метод [PDOStatement::fetch()](pdostatement.fetch.html)

### Список параметрів

`column`

Номер стовпця, дані якого потрібно витягти. Нумерація починається з 0. Якщо параметр не встановлено, **PDOStatement::fetchColumn()** обере дані першого стовпця.

### Значення, що повертаються

**PDOStatement::fetchColumn()** повертає значення одного стовпця наступного рядка результуючого набору або \*\*`false`\*\*якщо більше немає рядків.

**Увага**

При використанні **PDOStatement::fetchColumn()** для отримання даних з результуючого набору неможливо отримати значення іншого стовпця того ж рядка.

### Приклади

**Приклад #1 Отримання значення першого стовпця наступного рядка**

```php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

print("Получение значения первого столбца первой строки:\n");
$result = $sth->fetchColumn();
print("name = $result\n");

print("Получение значения второго столбца второй строки:\n");
$result = $sth->fetchColumn(1);
print("colour = $result\n");
?>
```

Результат виконання цього прикладу:

```
Получение значения первого столбца первой строки:
name = lemon
Получение значения второго столбца второй строки:
colour = red
```

### Дивіться також

-   [PDO::query()](pdo.query.html) - готує та виконує вираз SQL без заповнювачів
-   [PDOStatement::fetch()](pdostatement.fetch.html) - Вилучення наступного рядка з результуючого набору
-   [PDOStatement::fetchAll()](pdostatement.fetchall.html) - Вибирає рядки, що залишилися, з набору результатів
-   [PDO::prepare()](pdo.prepare.html) - готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::setFetchMode()](pdostatement.setfetchmode.html) - Встановлює режим вибірки за промовчанням для об'єкта запиту