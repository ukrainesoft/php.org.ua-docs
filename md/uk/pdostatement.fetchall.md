---
navigation:
  - pdostatement.fetch.md: '« PDOStatement::fetch'
  - pdostatement.fetchcolumn.md: 'PDOStatement::fetchColumn »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::fetchAll'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::fetchAll

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

PDOStatement::fetchAll — Вибирає рядки, що залишилися, з набору результатів

### Опис

```methodsynopsis
public PDOStatement::fetchAll(int $mode = PDO::FETCH_DEFAULT): array
```

```methodsynopsis
public PDOStatement::fetchAll(int $mode = PDO::FETCH_COLUMN, int $column): array
```

```methodsynopsis
public PDOStatement::fetchAll(int $mode = PDO::FETCH_CLASS, string $class, ?array $constructorArgs): array
```

```methodsynopsis
public PDOStatement::fetchAll(int $mode = PDO::FETCH_FUNC, callable $callback): array
```

### Список параметрів

`mode`

Визначає вміст масиву, що повертається. Докладніше можна дізнатися з документації до методу [PDOStatement::fetch()](pdostatement.fetch.md)По умолчанию параметр принимает значение\*\*`PDO::ATTR_DEFAULT_FETCH_MODE`\*\* (яке у свою чергу має умовчання **`PDO::FETCH_BOTH`**) .

Щоб вибрати значення лише одного стовпця, передайте як значення цього параметра константу \*\*`PDO::FETCH_COLUMN`\*\*С помощью параметра`column` можна встановити стовпець, з якого потрібно витягти дані.

Якщо потрібно витягти лише унікальні рядки одного стовпця, потрібно передати побітове АБО констант **`PDO::FETCH_COLUMN`** і **`PDO::FETCH_UNIQUE`**

Щоб отримати асоціативний масив рядків, згрупований за значеннями певного стовпця, потрібно передати побітове АБО констант **`PDO::FETCH_COLUMN`** і **`PDO::FETCH_GROUP`**

Наступні параметри динамічні і залежать від режиму вибірки. Вони не можуть використовуватися разом із іменованими параметрами.

`column`

Використовується з **`PDO::FETCH_COLUMN`**. Повертає зазначений стовпець з індексом, що починається з 0.

`class`

Використовується з **`PDO::FETCH_CLASS`**. Повертає екземпляри зазначеного класу, зіставляючи стовпці кожного рядка із іменованими властивостями класу.

`constructorArgs`

Аргументи конструктора користувача класу, коли параметр `mode`равен\*\*`PDO::FETCH_CLASS`\*\*

`callback`

Використовується з **`PDO::FETCH_FUNC`**. Повертає результати виклику вказаної функції, використовуючи стовпці кожного рядка як параметри виклику.

### Значення, що повертаються

Метод**PDOStatement::fetchAll()** повертає масив, що містить всі рядки результуючого набору. Масив представляє кожен рядок у вигляді масиву значень одного стовпця, або у вигляді об'єкта, імена властивостей якого збігаються з іменами стовпців.

Використання цього для вилучення рядків великих результуючих наборів може згубно позначитися на продуктивності системи та мережевих ресурсів. Замість отримання всіх даних та їх обробки в PHP рекомендується використовувати вбудовані засоби СУБД. Наприклад, використання виразів WHERE та ORDER BY мови SQL може зменшити розмір результуючого набору.

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод тепер завжди повертає масив (array), раніше у разі виникнення помилки могло повертатися **`false`** |

### Приклади

**Приклад #1 Вилучення всіх рядків результуючого набору, що залишилися.**

```php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* Извлечение всех оставшихся строк результирующего набора */
print "Извлечение всех оставшихся строк результирующего набора:\n";
$result = $sth->fetchAll();
print_r($result);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Извлечение всех оставшихся строк результирующего набора:
Array
(
    [0] => Array
        (
            [name] => apple
            [0] => apple
            [colour] => red
            [1] => red
        )

    [1] => Array
        (
            [name] => pear
            [0] => pear
            [colour] => green
            [1] => green
        )

    [2] => Array
        (
            [name] => watermelon
            [0] => watermelon
            [colour] => pink
            [1] => pink
        )
)
```

**Приклад #2 Вилучення всіх значень одного стовпця результуючого набору**

У наступному прикладі показано, як витягти з результуючого набору значення лише одного стовпця, навіть якщо рядки містять значення кількох стовпців.

```php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* Извлечение всех значений первого столбца */
$result = $sth->fetchAll(PDO::FETCH_COLUMN, 0);
var_dump($result);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array(3)
(
    [0] =>
    string(5) => apple
    [1] =>
    string(4) => pear
    [2] =>
    string(10) => watermelon
)
```

**Приклад #3 Угруповання рядків за значеннями одного стовпця**

У наведеному нижче прикладі показано, як отримати асоціативний масив рядків результуючого набору, згрупованих за значеннями зазначеного стовпця. Масив містить три ключі: значення `apple`и`pear` є масивами, що містять два різні кольори; в той же час `watermelon` буде масивом, що містить лише один колір.

```php
<?php
$insert = $dbh->prepare("INSERT INTO fruit(name, colour) VALUES (?, ?)");
$insert->execute(array('apple', 'green'));
$insert->execute(array('pear', 'yellow'));

$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* Группируем записи по значениям первого столбца */
var_dump($sth->fetchAll(PDO::FETCH_COLUMN|PDO::FETCH_GROUP));
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  ["apple"]=>
  array(2) {
    [0]=>
    string(5) "green"
    [1]=>
    string(3) "red"
  }
  ["pear"]=>
  array(2) {
    [0]=>
    string(5) "green"
    [1]=>
    string(6) "yellow"
  }
  ["watermelon"]=>
  array(1) {
    [0]=>
    string(5) "pink"
  }
}
```

**Приклад #4 Створення об'єкта для кожного рядка**

У наступному прикладі показано поведінку методу у режимі вибірки **`PDO::FETCH_CLASS`**

```php
<?php
class fruit {
    public $name;
    public $colour;
}

$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

$result = $sth->fetchAll(PDO::FETCH_CLASS, "fruit");
var_dump($result);
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  object(fruit)#1 (2) {
    ["name"]=>
    string(5) "apple"
    ["colour"]=>
    string(5) "green"
  }
  [1]=>
  object(fruit)#2 (2) {
    ["name"]=>
    string(4) "pear"
    ["colour"]=>
    string(6) "yellow"
  }
  [2]=>
  object(fruit)#3 (2) {
    ["name"]=>
    string(10) "watermelon"
    ["colour"]=>
    string(4) "pink"
  }
  [3]=>
  object(fruit)#4 (2) {
    ["name"]=>
    string(5) "apple"
    ["colour"]=>
    string(3) "red"
  }
  [4]=>
  object(fruit)#5 (2) {
    ["name"]=>
    string(4) "pear"
    ["colour"]=>
    string(5) "green"
  }
}
```

**Приклад #5 Виклик функції для кожного рядка**

У наступному прикладі показано поведінку методу у режимі вибірки **`PDO::FETCH_FUNC`**

```php
<?php
function fruit($name, $colour) {
    return "{$name}: {$colour}";
}

$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

$result = $sth->fetchAll(PDO::FETCH_FUNC, "fruit");
var_dump($result);
?>
```

Висновок наведеного прикладу буде схожим на:

```
array(3) {
  [0]=>
  string(12) "apple: green"
  [1]=>
  string(12) "pear: yellow"
  [2]=>
  string(16) "watermelon: pink"
  [3]=>
  string(10) "apple: red"
  [4]=>
  string(11) "pear: green"
}
```

### Дивіться також

-   [PDO::query()](pdo.query.md) \- готує та виконує вираз SQL без заповнювачів
-   [PDOStatement::fetch()](pdostatement.fetch.md) \- Вилучення наступного рядка з результуючого набору
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) \- Повертає дані одного стовпця наступного рядка результуючого набору
-   [PDO::prepare()](pdo.prepare.md) \- готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::setFetchMode()](pdostatement.setfetchmode.md) \- Встановлює режим вибірки за промовчанням для об'єкта запиту
