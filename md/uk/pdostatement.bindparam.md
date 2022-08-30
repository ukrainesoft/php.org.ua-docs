Прив'язує параметр запиту до змінної

-   [« PDOStatement::bindColumn](pdostatement.bindcolumn.html)
    
-   [PDOStatement::bindValue »](pdostatement.bindvalue.html)
    
-   [PHP Manual](index.html)
    
-   [PDOStatement](class.pdostatement.html)
    
-   Прив'язує параметр запиту до змінної
    

# PDOStatement::bindParam

(PHP 5> = 5.1.0, PHP 7, PHP 8, PECL pdo> = 0.1.0)

PDOStatement::bindParam — Прив'язує параметр запиту до змінної

### Опис

```methodsynopsis
public PDOStatement::bindParam(    string|int $param,    mixed &$var,    int $type = PDO::PARAM_STR,    int $maxLength = 0,    mixed $driverOptions = null): bool
```

Зв'язує змінну PHP з іменованим або неіменованим параметром SQL-запиту, що готується. На відміну від [PDOStatement::bindValue()](pdostatement.bindvalue.html), змінна прив'язується за посиланням та її значення обчислюватиметься під час виклику [PDOStatement::execute()](pdostatement.execute.html)

У більшості випадків у запитах, що готуються, використовуються тільки вхідні параметри, тобто при побудові запиту доступ до них здійснюється тільки в режимі читання (можливе приведення відповідно до `type`). Тим не менш, деякі драйвери дозволяють запускати збережені процедури, які, у свою чергу, можуть повертати дані за допомогою вихідних параметрів. Часто такі параметри використовуються одночасно як вхідні і як вихідні.

### Список параметрів

`param`

Ідентифікатор параметра. Для запитів, що готуються, з іменованими параметрами це буде ім'я у вигляді :name. Якщо використовуються неіменовані параметри (знаки питання?), це буде позиція псевдозмінної в запиті (починаючи з 1).

`var`

Ім'я змінної PHP, яку потрібно прив'язати до SQL-запиту.

`type`

Явно заданий тип даних параметра. Тип задається однією з [констант`PDO::PARAM_*`](pdo.constants.html). Якщо параметр використовується, у тому числі для виведення інформації з процедури, що зберігається, до значення аргументу `type` необхідно додати **`PDO::PARAM_INPUT_OUTPUT`**, використовуючи оператор побітове АБО.

`maxLength`

Розмір типу даних. Щоб вказати, що параметр використовується для виведення даних із процедури, необхідно явно задати його розмір. Має значення, тільки якщо параметр `type` встановлено значення **`PDO::PARAM_INPUT_OUTPUT`**

`driverOptions`

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
$sth->bindParam('calories', $calories, PDO::PARAM_INT);
/* Имена также могут начинаться с двоеточия ":" (необязательно) */
$sth->bindParam(':colour', $colour, PDO::PARAM_STR);
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
$sth->bindParam(1, $calories, PDO::PARAM_INT);
$sth->bindParam(2, $colour, PDO::PARAM_STR);
$sth->execute();
?>
```

**Приклад #3 Виклик процедури, що зберігається з INOUT-параметром**

```php
<?php
/* Вызов хранимой процедуры с INOUT-параметром */
$colour = 'red';
$sth = $dbh->prepare('CALL puree_fruit(?)');
$sth->bindParam(1, $colour, PDO::PARAM_STR|PDO::PARAM_INPUT_OUTPUT, 12);
$sth->execute();
print("После приготовления фруктового пюра, цвет - $colour");
?>
```

### Дивіться також

-   [PDO::prepare()](pdo.prepare.html) - готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::execute()](pdostatement.execute.html) - Запускає підготовлений запит на виконання
-   [PDOStatement::bindValue()](pdostatement.bindvalue.html) - Зв'язує параметр із заданим значенням