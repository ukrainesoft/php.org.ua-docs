Зв'язує параметр із заданим значенням

-   [« PDOStatement::bindParam](pdostatement.bindparam.html)
    
-   [PDOStatement::closeCursor »](pdostatement.closecursor.html)
    
-   [PHP Manual](index.html)
    
-   [PDOStatement](class.pdostatement.html)
    
-   Зв'язує параметр із заданим значенням
    

# PDOStatement::bindValue

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 1.0.0)

PDOStatement::bindValue — Зв'язує параметр із заданим значенням

### Опис

```methodsynopsis
public PDOStatement::bindValue(string|int $param, mixed $value, int $type = PDO::PARAM_STR): bool
```

Задає значення іменованої чи неіменованої псевдозмінної у підготовленому SQL-запиті.

### Список параметрів

`param`

Ідентифікатор запиту. Для запитів, що готуються, з іменованими параметрами це буде ім'я у вигляді :name. Якщо використовуються неіменовані параметри (знаки питання?), це буде позиція псевдозмінної в запиті (починаючи з 1).

`value`

Значення, яке потрібно прив'язати до параметра.

`type`

Явно заданий тип даних параметра. Тип задається однією з [констант`PDO::PARAM_*`](pdo.constants.html)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Виконання підготовленого запиту з іменованими псевдозмінними**

```php
<?php
/* Выполнение запроса с привязкой PHP-переменных */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');
$sth->bindValue('calories', $calories, PDO::PARAM_INT);
/* Имена также могут начинаться с двоеточия ":" (необязательно) */
$sth->bindValue(':colour', $colour, PDO::PARAM_STR);
$sth->execute();
?>
```

**Приклад #2 Виконання підготовленого запиту з неназваними псевдозмінними (?)**

```php
<?php
/* Выполнение запроса с привязкой PHP-переменных */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindValue(1, $calories, PDO::PARAM_INT);
$sth->bindValue(2, $colour, PDO::PARAM_STR);
$sth->execute();
?>
```

### Дивіться також

-   [PDO::prepare()](pdo.prepare.html) - готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::execute()](pdostatement.execute.html) - Запускає підготовлений запит на виконання
-   [PDOStatement::bindParam()](pdostatement.bindparam.html) - Прив'язує параметр запиту до змінної