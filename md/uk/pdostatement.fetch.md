---
navigation:
  - pdostatement.execute.md: '« PDOStatement::execute'
  - pdostatement.fetchall.md: 'PDOStatement::fetchAll »'
  - index.md: PHP Manual
  - class.pdostatement.md: PDOStatement
title: 'PDOStatement::fetch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# PDOStatement::fetch

(PHP 5 >= 5.1.0, PHP 7, PHP 8, PECL pdo >= 0.1.0)

PDOStatement::fetch — Витяг наступного рядка з результуючого набору

### Опис

```methodsynopsis
public PDOStatement::fetch(int $mode = PDO::FETCH_DEFAULT, int $cursorOrientation = PDO::FETCH_ORI_NEXT, int $cursorOffset = 0): mixed
```

Витягує наступний рядок з результуючого набору об'єкта PDOStatement. Параметр `mode` визначає, як PDO поверне цей рядок.

### Список параметрів

`mode`

Визначає, в якому вигляді наступний рядок буде повернено в метод, що викликає. Це може бути одна з констант `PDO::FETCH_*`По умолчанию`PDO::ATTR_DEFAULT_FETCH_MODE` (що рівносильно `PDO::FETCH_BOTH`

-   `PDO::FETCH_ASSOC`: повертає масив, індексований іменами стовпців результуючого набору
    
-   `PDO::FETCH_BOTH`(за замовчуванням): повертає масив, індексований іменами шпальт результуючого набору, а також їх номерами (починаючи з 0)
    
-   `PDO::FETCH_BOUND`: повертає\*\*`true`\*\*і надає значення стовпців результуючого набору змінним PHP, які були прив'язані до цих стовпців методом[PDOStatement::bindColumn()](pdostatement.bindcolumn.md)
    
-   `PDO::FETCH_CLASS`: створює та повертає об'єкт запитаного класу, присвоюючи значення стовпців результуючого набору іменованим властивостям класу, і потім викликає конструктор, якщо не заданий`PDO::FETCH_PROPS_LATE`. Якщо `mode`включає атрибут PDO::FETCH\_CLASSTYPE (наприклад,`PDO::FETCH_CLASS | PDO::FETCH_CLASSTYPE`), то ім'я класу, від якого потрібно створити об'єкт, буде взято з першого стовпця.
    
-   `PDO::FETCH_INTO`: оновлює існуючий об'єкт запитаного класу, присвоюючи значення стовпців результуючого набору іменованим властивостям об'єкта
    
-   `PDO::FETCH_LAZY`: комбінує`PDO::FETCH_BOTH`и`PDO::FETCH_OBJ` та повертає об'єкт [PDORow](class.pdorow.md)що створює імена властивостей об'єкта в міру доступу до них.
    
-   `PDO::FETCH_NAMED`: повертає масив такого ж виду, як і`PDO::FETCH_ASSOC`але якщо є кілька полів з однаковим ім'ям, то значенням з цим ключем буде масив з усіма значеннями з рядів, в яких це поле вказано.
    
-   `PDO::FETCH_NUM`: повертає масив, індексований номерами стовпців (починаючи з 0)
    
-   `PDO::FETCH_OBJ`: створює анонімний об'єкт із властивостями, що відповідають іменам стовпців результуючого набору
    
-   `PDO::FETCH_PROPS_LATE`: якщо використовується з`PDO::FETCH_CLASS`, конструктор класу буде викликано перед призначенням властивостей значень стовпців.
    

`cursorOrientation`

Для об'єктів PDOStatement, що представляють курсор, що прокручується, цей параметр визначає, який рядок буде повертатися в викликаючий метод. Значенням параметра має бути одна з констант `PDO::FETCH_ORI_*`, по умолчанию`PDO::FETCH_ORI_NEXT`. Щоб запросити курсор, що прокручується, для запиту PDOStatement, необхідно задати атрибут `PDO::ATTR_CURSOR`со значением`PDO::CURSOR_SCROLL`во время подготовки запроса методом[PDO::prepare()](pdo.prepare.md)

`cursorOffset`

Для об'єктів PDOStatement, що представляють курсор, що прокручується, параметр `cursorOrientation` яких набуває значення `PDO::FETCH_ORI_ABS`, Ця величина означає абсолютний номер рядка, яку необхідно витягти з результуючого набору.

Для об'єктів PDOStatement, що представляють курсор, що прокручується, параметр `cursorOrientation` яких набуває значення `PDO::FETCH_ORI_REL`, ця величина вказує, який рядок щодо поточного положення курсору буде вилучено функцією **PDOStatement::fetch()**

### Значення, що повертаються

У разі успішного виконання функції значення, що повертається, залежить від режиму вибірки. У разі виникнення помилки або якщо немає рядків, функція повертає **`false`**

### Помилки

Видає помилку рівня **`E_WARNING`**, якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_WARNING`**

Викидає виняток [PDOException](class.pdoexception.md), якщо атрибуту **`PDO::ATTR_ERRMODE`**установлено значение**`PDO::ERRMODE_EXCEPTION`**

### Приклади

**Приклад #1 Вилучення рядків у різних режимах вибірки**

```php
<?php
$sth = $dbh->prepare("SELECT name, colour FROM fruit");
$sth->execute();

/* Приклады различных режимов работы PDOStatement::fetch */
print "PDO::FETCH_ASSOC: ";
print "Возвращаем следующую строку в виде массива, индексированного именами столбцов\n";
$result = $sth->fetch(PDO::FETCH_ASSOC);
print_r($result);
print "\n";

print "PDO::FETCH_BOTH: ";
print "Возвращаем следующую строку в виде массива, индексированного как именами столбцов, так и их номерами\n";
$result = $sth->fetch(PDO::FETCH_BOTH);
print_r($result);
print "\n";

print "PDO::FETCH_LAZY: ";
print "Возвращаем следующую строку в виде объекта класса PDORow с именами столбцов в качестве свойств\n";
$result = $sth->fetch(PDO::FETCH_LAZY);
print_r($result);
print "\n";

print "PDO::FETCH_OBJ: ";
print "Возвращаем следующую строку в виде анонимного объекта со свойствами, соответствующими столбцам\n";
$result = $sth->fetch(PDO::FETCH_OBJ);
print $result->name;
print "\n";
?>
```

Результат виконання наведеного прикладу:

```
PDO::FETCH_ASSOC: Возвращаем следующую строку в виде массива, индексированного именами столбцов
Array
(
    [name] => apple
    [colour] => red
)

PDO::FETCH_BOTH: Возвращаем следующую строку в виде массива, индексированного как именами столбцов, так и их номерами
Array
(
    [name] => banana
    [0] => banana
    [colour] => yellow
    [1] => yellow
)

PDO::FETCH_LAZY: Возвращаем следующую строку в виде анонимного объекта со свойствами, соответствующими столбцам
PDO::FETCH_LAZY: Возвращаем следующую строку в виде объекта класса PDORow с именами столбцов в качестве свойств
PDORow Object
(
    [name] => orange
    [colour] => orange
)

PDO::FETCH_OBJ: Возвращаем следующую строку в виде анонимного объекта со свойствами, соответствующими столбцам
kiwi
```

**Приклад #2 Вибірка рядків засобами курсору, що прокручується.**

```php
<?php
function readDataForwards($dbh) {
    $sql = 'SELECT hand, won, bet FROM mynumbers ORDER BY BET';
    $stmt = $dbh->prepare($sql, array(PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL));
    $stmt->execute();
    while ($row = $stmt->fetch(PDO::FETCH_NUM, PDO::FETCH_ORI_NEXT)) {
        $data = $row[0] . "\t" . $row[1] . "\t" . $row[2] . "\n";
        print $data;
    }
}
function readDataBackwards($dbh) {
    $sql = 'SELECT hand, won, bet FROM mynumbers ORDER BY bet';
    $stmt = $dbh->prepare($sql, array(PDO::ATTR_CURSOR => PDO::CURSOR_SCROLL));
    $stmt->execute();
    $row = $stmt->fetch(PDO::FETCH_NUM, PDO::FETCH_ORI_LAST);
    do {
        $data = $row[0] . "\t" . $row[1] . "\t" . $row[2] . "\n";
        print $data;
    } while ($row = $stmt->fetch(PDO::FETCH_NUM, PDO::FETCH_ORI_PRIOR));
}

print "Читаем в прямой последовательности:\n";
readDataForwards($conn);

print "Читаем в обратной последовательности:\n";
readDataBackwards($conn);
?>
```

Результат виконання наведеного прикладу:

```
Читаем в прямой последовательности:
21    10    5
16    0     5
19    20    10

Читаем в обратной последовательности:
19    20    10
16    0     5
21    10    5
```

**Приклад #3 Порядок конструкторів**

Якщо об'єкти забираються за допомогою `PDO::FETCH_CLASS`, спочатку надаються властивості об'єкта, а потім викликається конструктор об'єкта. Якщо також задано `PDO::FETCH_PROPS_LATE`, цей порядок змінюється на зворотний.

```php
<?php
class Person
{
    private $name;

    public function __construct()
    {
        $this->tell();
    }

    public function tell()
    {
        if (isset($this->name)) {
            echo "Я {$this->name}.\n";
        } else {
            echo "У меня ещё нет имени.\n";
        }
    }
}

$sth = $dbh->query("SELECT * FROM people");
$sth->setFetchMode(PDO::FETCH_CLASS, 'Person');
$person = $sth->fetch();
$person->tell();
$sth->setFetchMode(PDO::FETCH_CLASS|PDO::FETCH_PROPS_LATE, 'Person');
$person = $sth->fetch();
$person->tell();
?>
```

Висновок наведеного прикладу буде схожим на:

```
Я - Alice.
Я Alice.
У меня ещё нет имени.
Я Bob.
```

### Дивіться також

-   [PDO::prepare()](pdo.prepare.md) \- готує запит до виконання та повертає пов'язаний із цим запитом об'єкт
-   [PDOStatement::execute()](pdostatement.execute.md) \- Запускає підготовлений запит на виконання
-   [PDOStatement::fetchAll()](pdostatement.fetchall.md) \- Вибирає рядки, що залишилися, з набору результатів
-   [PDOStatement::fetchColumn()](pdostatement.fetchcolumn.md) \- Повертає дані одного стовпця наступного рядка результуючого набору
-   [PDOStatement::fetchObject()](pdostatement.fetchobject.md) \- Витягує наступний рядок і повертає його у вигляді об'єкта
-   [PDOStatement::setFetchMode()](pdostatement.setfetchmode.md) \- Встановлює режим вибірки за промовчанням для об'єкта запиту
