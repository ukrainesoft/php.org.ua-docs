- [« PDOStatement::fetch](pdostatement.fetch.md)
- [PDOStatement::fetchColumn »](pdostatement.fetchcolumn.md)

- [PHP Manual](index.md)
- [PDOStatement](class.pdostatement.md)
- Вибирає рядки з набору результатів, що залишилися.

# PDOStatement::fetchAll

(PHP 5 = 5.1.0, PHP 7, PHP 8, PECL pdo = 0.1.0)

PDOStatement::fetchAll — Вибирає рядки, що залишилися, з набору
результатів

### Опис

public **PDOStatement::fetchAll**(int `$mode` = PDO::FETCH_DEFAULT):
array

public **PDOStatement::fetchAll**(int `$mode` = PDO::FETCH_COLUMN, int
`$column`): array

public **PDOStatement::fetchAll**(int `$mode` = PDO::FETCH_CLASS, string
`$class`, ?array `$constructorArgs`): array

public **PDOStatement::fetchAll**(int `$mode` = PDO::FETCH_FUNC,
[callable](language.types.callable.md) `$callback`): array

### Список параметрів

`mode`
Визначає вміст масиву, що повертається. Докладніше можна дізнатися з
документації до методу [PDOStatement::fetch()](pdostatement.fetch.md).
За замовчуванням параметр приймає значення
**`PDO::ATTR_DEFAULT_FETCH_MODE`** (яке в свою чергу має
замовчування **`PDO::FETCH_BOTH`**)

Щоб отримати значення лише одного стовпця, передайте як
значення цього параметра константу **`PDO::FETCH_COLUMN`**. За допомогою
параметра `column` можна задати стовпець, з якого потрібно витягти
дані.

Якщо потрібно витягти лише унікальні рядки одного стовпця, потрібно
передати побітове АБО констант **`PDO::FETCH_COLUMN`** та
**`PDO::FETCH_UNIQUE`**.

Щоб отримати асоціативний масив рядків, згрупований за значеннями
певного стовпця, потрібно передати побітове АБО констант
**`PDO::FETCH_COLUMN`** та **`PDO::FETCH_GROUP`**.

`args`
Сенс цього аргументу залежить від значення параметра `mode`:

- **`PDO::FETCH_COLUMN`**: Буде повернено вказаний стовпець.
Індексація стовпців починається з 0.

- **`PDO::FETCH_CLASS`**: Буде створено та повернено новий об'єкт
вказаного класу. Властивості об'єкта будуть присвоєні значення
стовпців, імена яких збігатимуться з іменами властивостей.

- **`PDO::FETCH_FUNC`**: Будуть повернені результати викликів вказаної
функції. Дані кожного рядка результуючого набору будуть
передаватися у цю функцію.

`constructorArgs`
Аргументи конструктора класу. Для випадків, коли параметру `mode`
надано значення **`PDO::FETCH_CLASS`**.

### Значення, що повертаються

**PDOStatement::fetchAll()** повертає масив, що містить усі
рядки результуючого набору, що залишилися. Масив представляє кожну
рядок або у вигляді масиву значень одного стовпця, або у вигляді об'єкта,
імена властивостей якого збігаються з іменами стовпців.

Використання цього методу для вилучення рядків великих результатів
наборів може згубно позначитися на продуктивності системи та мережевих
ресурсів. Замість вилучення всіх даних та їх обробки в PHP
рекомендується використовувати вбудовані засоби СУБД. Наприклад,
використання виразів WHERE та ORDER BY мови SQL може зменшити
розміри результуючого набору.

### Список змін

| Версія | Опис                                                                                                     |
| ------ | -------------------------------------------------------------------------------------------------------- |
| 8.0.0  | Метод тепер завжди повертає масив (array), раніше у разі виникнення помилки могло повертатися **false**. |

### Приклади

**Приклад #1 Вилучення всіх рядків результуючого набору**, що залишилися**

` <?php$sth = $dbh->prepare("SELECT name, colour FROM fruit");$sth->execute();/* Витягнення всіх залишилися рядків рухнастрок і      :
");$result = $sth->fetchAll();print_r($result);?> `

Результатом виконання цього прикладу буде щось подібне:

Вилучення всіх рядків результуючого набору:
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

**Приклад #2 Вилучення всіх значень одного стовпця результуючого
набору**

У наступному прикладі показано, як витягти з результуючого набору
значення лише одного стовпця, навіть якщо рядки містять значення
кількох стовпців.

` <?php$sth = $dbh->prepare("SELECT name, colour FROM fruit");$sth->execute();/*¦Вилучення всіх значень першого стовпця */$result = chs ::FETCH_COLUMN, 0);var_dump($result);?> `

Результатом виконання цього прикладу буде щось подібне:

Array(3)
(
[0] =>
string(5) => apple
[1] =>
string(4) => pear
[2] =>
string(10) => watermelon
)

**Приклад #3 Угруповання рядків за значеннями одного стовпця**

У наступному прикладі показано, як отримати асоціативний масив рядків
результуючого набору, що згруповано за значеннями зазначеного стовпця.
Масив містить три ключі: значення `apple` та `pear` є масивами,
що містять два різні кольори; в той же час `watermelon` буде масивом,
що містить лише один колір.

` <?php$insert = $dbh->prepare("INSERT INTO fruit(name, colour) VALUES (?, ?)");$insert->execute(array('apple', 'green'));$ insert->execute(array('pear', 'yellow'));$sth = $dbh->prepare("SELECT name, colour FROM fruit");$sth->execute();/* Групуємо записи за значеннями першого стовпця*/var_dump($sth->fetchAll(PDO::FETCH_COLUMN|PDO::FETCH_GROUP));?> `

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #4 Створення об'єкта для кожного рядка**

У наступному прикладі показано поведінку методу у режимі вибірки
**`PDO::FETCH_CLASS`**.

`<?phpclass fruit {    public $name; public $colour;}$sth = $dbh->prepare("SELECT name, colour FROM fruit");$sth->execute();$result = $sth->fetchAll(PDO::FETCH_CLASS, "fruit" ;var_dump($result);?> `

Результатом виконання цього прикладу буде щось подібне:

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

**Приклад #5 Виклик функції для кожного рядка**

У наступному прикладі показано поведінку методу у режимі вибірки
**`PDO::FETCH_FUNC`**.

` <?phpfunction fruit($name, $colour) {   return "{$name}: {$colour}";}$sth = $dbh->prepare("SELECT name, colour FROM fruit");$s execute();$result = $sth->fetchAll(PDO::FETCH_FUNC, "fruit");var_dump($result);?> `

Результатом виконання цього прикладу буде щось подібне:

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

### Дивіться також

- [PDO::query()](pdo.query.md) - Готує та виконує
вираз SQL без наповнювачів
- [PDOStatement::fetch()](pdostatement.fetch.md) - Вилучення
наступного рядка з результуючого набору
- [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) -
Повертає дані одного стовпця наступного рядка результуючого
набору
- [PDO::prepare()](pdo.prepare.md) - Підготовка запиту до
виконання та повертає пов'язаний з цим запитом об'єкт
- [PDOStatement::setFetchMode()](pdostatement.setfetchmode.md) -
Встановлює стандартний режим вибірки для об'єкта запиту
