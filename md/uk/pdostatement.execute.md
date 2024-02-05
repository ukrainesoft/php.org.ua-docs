---
navigation:
  - pdostatement.errorinfo.md: '« PDOStatement::errorInfo'
  - pdostatement.fetch.md: 'PDOStatement::fetch »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::execute'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::execute

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

PDOStatement::execute — Запускає підготовлений запит на виконання

### Опис

```methodsynopsis
public PDOStatement::execute(?array $params = null): bool
```

Запускає [підготовлений запит](pdo.prepared-statements.md). Якщо запит містить маркери параметрів (псевдозмінні), ви повинні:

-   викликати[PDOStatement::bindParam()](pdostatement.bindparam.md)и/или[PDOStatement::bindValue()](pdostatement.bindvalue.md), щоб зв'язати ці маркери, відповідно, зі змінними чи значеннями. Пов'язані змінні передають свої значення як вхідні дані та отримують вихідні значення
    
-   або передати масив значень лише на вхід
    

### Список параметрів

`params`

Масив значень містить стільки елементів, скільки параметрів заявлено в SQL-запиті. Усі значення будуть прийняті як такі, що мають тип **`PDO::PARAM_STR`**

Не можна прив'язати кілька значень одного параметра; наприклад, не можна прив'язати два значення до іменованого параметра у виразі IN().

Не можна прив'язати більше значень, ніж заявлено у запиті; якщо в масиві `params` більше елементів, ніж заявлено у SQL-запиті методом [PDO::prepare()](pdo.prepare.md), виконання запиту завершиться невдачею та буде викликана помилка.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Виконання підготовленого запиту з прив'язкою змінних та значень**

```php
<?php
/* Выполнение подготовленного запроса с привязкой переменных и значений */
$calories = 150;
$colour = 'gre';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour LIKE :colour');
$sth->bindParam('calories', $calories, PDO::PARAM_INT);
/* Имена также могут начинаться с двоеточия ":" (необязательно) */
$sth->bindValue(':colour', "%$colour%");
$sth->execute();
?>
```

**Приклад #2 Виконання підготовленого запиту з масивом іменованих значень**

```php
<?php
/* Выполнение подготовленного запроса с передачей массива входных значений */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->execute(array('calories' => $calories, 'colour' => $colour));
/* Ключи массива также могут начинаться с двоеточия ":" (необязательно) */
$sth->execute(array(':calories' => $calories, ':colour' => $colour));
?>
```

**Приклад #3 Виконання підготовленого запиту з масивом значень позицій**

```php
<?php
/* Выполнение подготовленного запроса с передачей массива входных значений */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->execute(array($calories, $colour));
?>
```

**Приклад #4 Виконання підготовленого запиту зі змінними, прив'язаними до позиційних заповнювачів**

```php
<?php
/* Выполнение подготовленного запроса с привязкой PHP переменных */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindParam(1, $calories, PDO::PARAM_INT);
$sth->bindParam(2, $colour, PDO::PARAM_STR, 12);
$sth->execute();
?>
```

**Приклад #5 Виконання підготовленого запиту з використанням масиву для вираження IN**

```php
<?php
/* Выполнение подготовленного запроса с использованием массива для выражения IN */
$params = array(1, 21, 63, 171);
/* Создаём строку из знаков вопроса (?) в количестве, равном количеству параметров */
$place_holders = implode(',', array_fill(0, count($params), '?'));

/*
    В этом Прикладе подготавливается запрос с достаточным количеством неименованных
    псевдопеременных (?) для каждого значения из массива $params. Когда запрос будет
    выполняться, эти знаки вопроса будут заменены на элементы массива. Это не то же
    самое, что использовать PDOStatement::bindParam(), где привязка осуществляется по
    ссылке на переменную. PDOStatement::execute() связывает параметры по значению.
*/
$sth = $dbh->prepare("SELECT id, name FROM contacts WHERE id IN ($place_holders)");
$sth->execute($params);
?>
```

### Примітки

> **Зауваження** :
> 
> Для деяких драйверів потрібно [закривати курсор](pdostatement.closecursor.md), перш ніж виконувати наступний запит.

### Дивіться також

-   [PDO::prepare()](pdo.prepare.md) \- готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::bindParam()](pdostatement.bindparam.md) \- Прив'язує параметр запиту до змінної
-   [PDOStatement::fetch()](pdostatement.fetch.md) \- Вилучення наступного рядка з результуючого набору
-   [PDOStatement::fetchAll()](pdostatement.fetchall.md) \- Вибирає рядки, що залишилися, з набору результатів
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) \- Повертає дані одного стовпця наступного рядка результуючого набору
