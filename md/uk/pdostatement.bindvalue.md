---
navigation:
  - pdostatement.bindparam.md: '« PDOStatement::bindParam'
  - pdostatement.closecursor.md: 'PDOStatement::closeCursor »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::bindValue'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::bindValue

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 1.0.0)

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

Явно заданий тип даних параметра. Тип задається однією з [констант`PDO::PARAM_*`](pdo.constants.md)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Виконання підготовленого запиту з іменованими псевдозмінними**

```php
<?php
/* Выполнение запроса с привязкой PHP-переменных */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < :calories AND colour = :colour');

/* Устанавливает значение параметра, используя его имя */
$sth->bindValue('calories', $calories, PDO::PARAM_INT);
/* По желанию, в именах параметров можно также ставить двоеточие ":" */
$sth->bindValue(':colour', $colour, PDO::PARAM_STR);
$sth->execute();
?>
```

**Приклад #2 Виконання підготовленого запиту з неназваними псевдозмінними (?)**

```php
<?php
/* Выполнение запроса с привязкой PHP-переменных */
$calories = 150;
$colour = 'red';
$sth = $dbh->prepare('SELECT name, colour, calories
    FROM fruit
    WHERE calories < ? AND colour = ?');
$sth->bindValue(1, $calories, PDO::PARAM_INT);
$sth->bindValue(2, $colour, PDO::PARAM_STR);
$sth->execute();
?>
```

### Дивіться також

-   [PDO::prepare()](pdo.prepare.md) \- готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::execute()](pdostatement.execute.md) \- Запускає підготовлений запит на виконання
-   [PDOStatement::bindParam()](pdostatement.bindparam.md) \- Прив'язує параметр запиту до змінної
