Нова функціональність

-   [« Зміни, що ламають зворотну сумісність](migration70.incompatible.html)
    
-   [Функціональність, оголошена застарілою в PHP 7.0.x](migration70.deprecated.html)
    
-   [PHP Manual](index.html)
    
-   [Миграция с PHP 5.6.x на PHP 7.0.x](migration70.html)
    
-   Нова функціональність
    

## Нова функціональність

### Оголошення скалярних типів

[Оголошення скалярних типів](language.types.declarations.html) введена у двох варіантах: примусовий (за умовчанням) та суворий. Наступні типи можуть бути використані для оголошення параметрів (в обох варіантах): рядки (string), цілі (`int`), числа з плаваючою точкою (float) та логічні значення (`bool`). Вони доповнюють аргументи інших типів, введених у PHP 5: імена класів, інтерфейсів, array та [callable](language.types.callable.html)

```php
<?php
// Принудительный режим
function sumOfInts(int ...$ints)
{
    return array_sum($ints);
}

var_dump(sumOfInts(2, '3', 4.1));
```

Результат виконання цього прикладу:

```
int(9)
```

Для встановлення строгого режиму, на початку файлу необхідно помістити одну директиву [`declare`](control-structures.declare.html). Це означає, що строгість оголошення скалярних типів працює лише на рівні файла і зачіпає весь інший код. Ця директива зачіпає не тільки оголошення параметрів, але і значення функцій, що повертаються (дивіться [оголошення типу, що повертається](language.types.declarations.html)), вбудовані функції PHP та функції завантажених модулів.

Детальну документацію та приклади використання читайте у розділі [декларация типов](language.types.declarations.html)

### Оголошення значень, що повертаються

У PHP 7 додано підтримку [оголошення типу, що повертається](language.types.declarations.html). Аналогічно як і [оголошення типів аргументів](language.types.declarations.html), оголошення типу значення, що повертається вказує, значення якого типу повинна повернути функція. Для оголошення типу значення, що повертається доступні все ті ж [типи](language.types.declarations.html)що для оголошення типів аргументів.

```php
<?php

function arraysSum(array ...$arrays): array
{
    return array_map(function(array $array): int {
        return array_sum($array);
    }, $arrays);
}

print_r(arraysSum([1,2,3], [4,5,6], [7,8,9]));
```

Результат виконання цього прикладу:

```
Array
(
    [0] => 6
    [1] => 15
    [2] => 24
)
```

Повну документацію та приклади використання читайте у розділі про [оголошення типу, що повертається](language.types.declarations.html)

### Оператор об'єднання з null

Було додано оператор об'єднання з null (`??`), що є синтаксичним цукром для досить поширеної дії, коли спільно використовуються тернарний оператор та функція [isset()](function.isset.html). Він повертає перший операнд, якщо він заданий і не дорівнює **`null`**, а у протилежному випадку повертає другий операнд.

```php
<?php
// Извлекаем значение $_GET['user'], а если оно не задано,
// то возвращаем 'nobody'
$username = $_GET['user'] ?? 'nobody';
// Это идентично следующему коду:
$username = isset($_GET['user']) ? $_GET['user'] : 'nobody';

// Данный оператор можно использовать в цепочке.
// В этом примере мы сперва проверяем, задан ли $_GET['user'], если нет,
// то проверяем $_POST['user'], и если он тоже не задан, то присваеваем 'nobody'.
$username = $_GET['user'] ?? $_POST['user'] ?? 'nobody';
?>
```

### Оператор spaceship (космічний корабель)

Цей оператор призначений для порівняння двох виразів. Він повертає -1, 0 або 1, якщо $a, відповідно, менше, дорівнює або більше ніж $b. Порівняння проводиться відповідно до [правилами порівняння типів](types.comparisons.html) PHP.

```php
<?php
// Целые числа
echo 1 <=> 1; // 0
echo 1 <=> 2; // -1
echo 2 <=> 1; // 1

// Числа с плавающей точкой
echo 1.5 <=> 1.5; // 0
echo 1.5 <=> 2.5; // -1
echo 2.5 <=> 1.5; // 1

// Строки
echo "a" <=> "a"; // 0
echo "a" <=> "b"; // -1
echo "b" <=> "a"; // 1
?>
```

### Визначення констант масивів за допомогою [define()](function.define.html)

Можна визначити константу типу array за допомогою функції [define()](function.define.html). У PHP 5.6 такі константи можна було задавати лише за допомогою [`const`](language.constants.syntax.html)

```php
<?php
define('ANIMALS', [
    'dog',
    'cat',
    'bird'
]);

echo ANIMALS[1]; // выводит "cat"
?>
```

### Анонімні класи

Додано підтримку анонімних класів за допомогою `new class`. Їх можна використовувати тоді, коли потрібен одноразовий клас і створювати повноцінний клас, а потім його об'єкт не має сенсу:

```php
<?php
interface Logger {
    public function log(string $msg);
}

class Application {
    private $logger;

    public function getLogger(): Logger {
         return $this->logger;
    }

    public function setLogger(Logger $logger) {
         $this->logger = $logger;
    }
}

$app = new Application;
$app->setLogger(new class implements Logger {
    public function log(string $msg) {
        echo $msg;
    }
});

var_dump($app->getLogger());
?>
```

Результат виконання цього прикладу:

```
object(class@anonymous)#2 (0) {
}
```

Детальну документацію та приклади використання читайте у розділі про [анонімні класи](language.oop5.anonymous.html)

### Синтаксис кодування Unicode

Він приймає шістнадцятковий код Unicode і записуємо його у форматі UTF-8 у подвійних лапках або форматі heredoc. Будь-який коректний код буде прийнято. Ведучі нулі за бажанням.

```php
echo "\u{aa}";
echo "\u{0000aa}";
echo "\u{9999}";
```

Результат виконання цього прикладу:

```
ª
ª (То же самое, что и первый вариант, но с ведущими нулями)
香
```

### [Closure::call()](closure.call.html)

[Closure::call()](closure.call.html) є більш продуктивним та коротким способом тимчасового зв'язування області дії об'єкта із замиканням та його викликом.

```php
<?php
class A {private $x = 1;}

// До PHP 7
$getX = function() {return $this->x;};
$getXCB = $getX->bindTo(new A, 'A'); // промежуточное замыкание
echo $getXCB();

// PHP 7+
$getX = function() {return $this->x;};
echo $getX->call(new A);
```

Результат виконання цього прикладу:

```
1
1
```

### [unserialize()](function.unserialize.html) з фільтрацією

Ця функціональність забезпечує більш високий рівень безпеки під час десеріалізації об'єктів з неперевіреними даними. Це дозволяє запобігти можливій ін'єкції коду, дозволяючи розробнику використовувати білий список класів для десеріалізації.

```php
<?php

// Преобразование всех объектов в __PHP_Incomplete_Class
$data = unserialize($foo, ["allowed_classes" => false]);

// Преобразование всех объектов, кроме MyClass и MyClass2 в __PHP_Incomplete_Class
$data = unserialize($foo, ["allowed_classes" => ["MyClass", "MyClass2"]]);

// Поведение по умолчанию принимает все классы (можно просто не задавать второй аргумент)
$data = unserialize($foo, ["allowed_classes" => true]);
```

### [IntlChar](class.intlchar.html)

Новий клас [IntlChar](class.intlchar.html) додає нову функціональність ICU. Клас визначає кілька статичних методів та констант для маніпулювання символами Unicode.

```php
<?php

printf('%x', IntlChar::CODEPOINT_MAX);
echo IntlChar::charName('@');
var_dump(IntlChar::ispunct('!'));
```

Результат виконання цього прикладу:

```
10ffff
COMMERCIAL AT
bool(true)
```

Для використання цього класу необхідно встановити модуль [Intl](book.intl.html)

### Очікування

[Ожидания](function.assert.html#function.assert.expectations) є покращеною, обернено сумісною версією старої функції [assert()](function.assert.html). Вони дозволяють робити припущення з нульовою вартістю в промисловому коді і надають можливість викидати винятки в разі провалу очікування.

Разом з тим, що старе API підтримується, [assert()](function.assert.html) тепер є мовною конструкцією, що приймає першим аргументом висловлювання, а не лише рядки (string) для оцінки чи логічні значення (bool) для перевірки.

```php
<?php
ini_set('assert.exception', 1);

class CustomError extends AssertionError {}

assert(false, new CustomError('Сообщение об ошибке'));
?>
```

Результат виконання цього прикладу:

```
Fatal error: Uncaught CustomError: Сообщение об ошибке
```

Детальний опис цього функціоналу, а також інструкції для його конфігурування для тестових та промислових середовищ читайте у секції [Ожидания](function.assert.html#function.assert.expectations) розділу, присвяченому [assert()](function.assert.html)

### Групові оголошення `use`

Класи, функції та константи імпортовані з одного і того ж [`namespace`](language.namespaces.definition.html), тепер можна групувати в одному операторі [`use`](language.namespaces.importing.html)

```php
<?php
// До PHP 7
use some\namespace\ClassA;
use some\namespace\ClassB;
use some\namespace\ClassC as C;

use function some\namespace\fn_a;
use function some\namespace\fn_b;
use function some\namespace\fn_c;

use const some\namespace\ConstA;
use const some\namespace\ConstB;
use const some\namespace\ConstC;

// PHP 7+
use some\namespace\{ClassA, ClassB, ClassC as C};
use function some\namespace\{fn_a, fn_b, fn_c};
use const some\namespace\{ConstA, ConstB, ConstC};
?>
```

### Вираз return у генераторах

Ця функціональність додана до генераторів, введених у PHP 5.5. Вона дозволяє використовувати оператор `return` в генераторах як остаточне значення, що повертається (повернення за посиланням неприпустимо). Це значення можна отримати за допомогою нового методу `Generator::getReturn()`, який можна використовувати тільки після того, як генератор повернув усі згенеровані значення.

```php
<?php

$gen = (function() {
    yield 1;
    yield 2;

    return 3;
})();

foreach ($gen as $val) {
    echo $val, PHP_EOL;
}

echo $gen->getReturn(), PHP_EOL;
```

Результат виконання цього прикладу:

```
1
2
3
```

Можливість явно отримувати остаточне значення генератора є дуже корисною, оскільки дозволяє клієнтському коду, що використовує генератор, отримувати та обробити останнє значення генератора, після якого точно нічого більше не буде. Це дуже простіше, ніж змушувати розробника перевіряти, чи останнє значення повернулося і якось особливо його обробляти.

### Делегація генератора

Тепер генератор може автоматично делегувати іншому генератору, об'єкту класу, що реалізує [Traversable](class.traversable.html) або масиву без необхідності писати додаткову обробку отриманих значень. Досягається це за допомогою конструкції [`yield from`](language.generators.syntax.html#control-structures.yield.from)

```php
<?php
function gen()
{
    yield 1;
    yield 2;
    yield from gen2();
}

function gen2()
{
    yield 3;
    yield 4;
}

foreach (gen() as $val)
{
    echo $val, PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
1
2
3
4
```

### Функція цілісного поділу [intdiv()](function.intdiv.html)

Нова функція [intdiv()](function.intdiv.html) виробляє цілий поділ операндів і повертає його результат.

```php
<?php
var_dump(intdiv(10, 3));
?>
```

Результат виконання цього прикладу:

```
int(3)
```

### Опції сесій

Тепер [sessionstart()](function.session-start.html) приймає масив опцій, які перевизначать [конфігураційні директиви сесії](session.configuration.html) встановлені у php.ini.

Також опції були розширені включеною за замовчуванням опцією [session.lazywrite](session.configuration.html#ini.session.lazy-write), яка говорить PHP про те, що файл сесії треба перезаписувати тільки якщо змінилися дані сесії, і опцією `read_and_close`, яку можна задати тільки через [sessionstart()](function.session-start.html) для того, щоб PHP закривав сесію відразу ж як прочитає її дані і не вносив до неї будь-яких змін.

Наприклад, для встановлення [session.cachelimiter](session.configuration.html#ini.session.cache-limiter) рівним `private` та негайного закриття сесії після читання її даних:

```php
<?php
session_start([
    'cache_limiter' => 'private',
    'read_and_close' => true,
]);
?>
```

### [pregreplacecallbackarray()](function.preg-replace-callback-array.html)

Нова функція [pregreplacecallbackarray()](function.preg-replace-callback-array.html) дозволяє писати чистіший код, коли потрібно використовувати функцію [pregreplacecallback()](function.preg-replace-callback.html). До PHP 7 при необхідності обробити різні регулярні вирази різними функціями доводилося для кожної такої обробки писати окремий виклик функції.

Тепер можна використовувати одну функцію, передаючи до неї асоціативний масив, ключами якого є регулярні вирази, а значеннями – функції зворотного виклику.

### Функції [CSPRNG](book.csprng.html)

Було додано дві нові кросплатформні функції для генерації криптографічно безпечних рядків і цілих чисел: [randombytes()](function.random-bytes.html) і [randomint()](function.random-int.html)

### Тепер функція [list()](function.list.html) завжди може розпаковувати об'єкти, що реалізують [ArrayAccess](class.arrayaccess.html)

Раніше функція [list()](function.list.html) не гарантувала коректну обробку об'єктів, що реалізують [ArrayAccess](class.arrayaccess.html). Тепер це виправлено.

### Інші зміни

-   Додано можливість доступу до методів та властивостей класу при клонуванні, тобто `(clone $foo)->bar()`