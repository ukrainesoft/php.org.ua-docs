---
navigation:
  - oop5.intro.md: '" Вступ'
  - language.oop5.properties.md: Властивості »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Основи
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Основи

### class

Кожне визначення класу починається з ключового слова `class`, Потім слідує ім'я класу, і далі пара фігурних дужок, які містять визначення властивостей і методів цього класу.

Ім'ям класу може бути будь-яке слово, за умови, що воно не входить до списку [зарезервованих слів](reserved.md) PHP починається з літери або символу підкреслення і за яким слідує будь-яка кількість букв, цифр або символів підкреслення. Якщо задати ці правила у вигляді регулярного виразу, то вийде таке вираз: `^[a-zA-Z_\x80-\xff][a-zA-Z0-9_\x80-\xff]*$`

Клас може містити власні [константи](language.oop5.constants.md) [змінні](language.oop5.properties.md) (звані властивостями) та функції (звані методами).

**Приклад #1 Просте визначення класу**

```php
<?php
class SimpleClass
{
    // объявление свойства
    public $var = 'значение по умолчанию';

    // объявление метода
    public function displayVar() {
        echo $this->var;
    }
}
?>
```

Псевдозмінна $this доступна в тому випадку, якщо метод був викликаний у контексті об'єкта. $this - значення об'єкта, що викликає.

**Увага**

Виклик нестатичного методу статично викликає помилку [Error](class.error.md). До PHP 8.0.0 це призвело б до повідомлення про старіння, і $this не було б визначено.

**Приклад #2 Деякі приклади псевдо-змінної $this**

```php
<?php
class A
{
    function foo()
    {
        if (isset($this)) {
            echo '$this определена (';
            echo get_class($this);
            echo ")\n";
        } else {
            echo "\$this не определена.\n";
        }
    }
}

class B
{
    function bar()
    {
        A::foo();
    }
}

$a = new A();
$a->foo();

A::foo();

$b = new B();
$b->bar();

B::bar();
?>
```

Результат виконання наведеного прикладу в PHP 7:

```
$this определена (A)

Deprecated: Non-static method A::foo() should not be called statically in %s  on line 27
$this не определена.

Deprecated: Non-static method A::foo() should not be called statically in %s  on line 20
$this не определена.

Deprecated: Non-static method B::bar() should not be called statically in %s  on line 32

Deprecated: Non-static method A::foo() should not be called statically in %s  on line 20
$this не определена.
```

Результат виконання наведеного прикладу в PHP 8:

```
$this определена (A)

Fatal error: Uncaught Error: Non-static method A::foo() cannot be called statically in %s :27
Stack trace:
#0 {main}
  thrown in %s  on line 27
```

#### Класи, доступні лише для читання

Починаючи з PHP 8.2.0, клас може бути позначений модифікатором readonly. Клас класу як readonly додасть [модифікатор readonly](language.oop5.properties.md#language.oop5.properties.readonly-properties) до кожної оголошеної властивості і запобігатиме створенню [динамічних властивостей](language.oop5.properties.md#language.oop5.properties.dynamic-properties). Більше того, неможливо додати їх підтримку за допомогою атрибуту [AllowDynamicProperties](class.allowdynamicproperties.md). Спроба зробити це призведе до помилки компіляції.

```php
<?php
#[\AllowDynamicProperties]
readonly class Foo {
}

// Fatal error: Cannot apply #[AllowDynamicProperties] to readonly class Foo
?>
```

Оскільки ні нетипізовані, ні статичні властивості не можуть бути позначені модифікатором `readonly`, класи, доступні тільки для читання також не можуть їх оголошувати:

```php
<?php
readonly class Foo
{
    public $bar;
}

// Fatal error: Readonly property Foo::$bar must have type
?>
```

```php
<?php
readonly class Foo
{
    public static int $bar;
}

// Fatal error: Readonly class Foo cannot declare static properties
?>
```

Клас readonly може бути [розширено](language.oop5.basic.md#language.oop5.basic.extends) тоді і тільки тоді, коли дочірній клас також є класом readonly.

### new

Для створення екземпляра класу використовується директива `new`. Новий об'єкт завжди буде створений, за винятком випадків, коли він містить [конструктор](language.oop5.decon.md), в якому визначено виклик [винятки](language.exceptions.md) у разі виникнення помилки. Рекомендується визначати класи до створення екземплярів (у деяких випадках це обов'язково).

Якщо з директивою `new` використовується рядок (string), що містить ім'я класу, буде створено новий екземпляр цього класу. Якщо ім'я знаходиться у просторі імен, воно має бути задано повністю.

> **Зауваження** :
> 
> У разі відсутності аргументів у конструктор класу круглі дужки після назви класу можна опустити.

**Приклад #3 Створення екземпляра класу**

```php
<?php
$instance = new SimpleClass();

// Это же можно сделать с помощью переменной:
$className = 'SimpleClass';
$instance = new $className(); // new SimpleClass()
?>
```

Починаючи з PHP 8.0.0, підтримується використання оператора `new` з довільними виразами. Це дозволяє створювати складніші екземпляри, якщо вираз представлений у вигляді рядка (string). Вирази мають бути поміщені у круглі дужки.

**Приклад #4 Створення екземпляра з використанням довільного виразу**

У цьому прикладі ми показуємо кілька варіантів допустимих довільних виразів, які є ім'ям класу. Приклад виклику функції, конкатенації рядків та константи **`::class`**

```php
<?php

class ClassA extends \stdClass {}
class ClassB extends \stdClass {}
class ClassC extends ClassB {}
class ClassD extends ClassA {}

function getSomeClass(): string
{
    return 'ClassA';
}

var_dump(new (getSomeClass()));
var_dump(new ('Class' . 'B'));
var_dump(new ('Class' . 'C'));
var_dump(new (ClassD::class));
?>
```

Результат виконання наведеного прикладу в PHP 8:

```
object(ClassA)#1 (0) {
}
object(ClassB)#1 (0) {
}
object(ClassC)#1 (0) {
}
object(ClassD)#1 (0) {
}
```

У контексті класу можна створити новий об'єкт через `new self`и`new parent`

Коли відбувається присвоєння вже існуючого екземпляра класу нової змінної, то ця змінна вказуватиме на цей самий екземпляр класу. Те саме відбувається і при передачі екземпляра класу в функцію. Копію вже створеного об'єкта можна створити через неї [клонування](language.oop5.cloning.md)

**Приклад #5 Привласнення об'єкта**

```php
<?php

$instance = new SimpleClass();

$assigned   =  $instance;
$reference  =& $instance;

$instance->var = '$assigned будет иметь это значение';

$instance = null; // $instance и $reference становятся null

var_dump($instance);
var_dump($reference);
var_dump($assigned);
?>
```

Результат виконання наведеного прикладу:

```
NULL
NULL
object(SimpleClass)#1 (1) {
   ["var"]=>
     string(30) "$assigned будет иметь это значение"
}
```

Створювати екземпляри об'єкта можна двома способами:

**Приклад #6 Створення нових об'єктів**

```php
<?php
class Test
{
    static public function getNew()
    {
        return new static;
    }
}

class Child extends Test
{}

$obj1 = new Test();
$obj2 = new $obj1;
var_dump($obj1 !== $obj2);

$obj3 = Test::getNew();
var_dump($obj3 instanceof Test);

$obj4 = Child::getNew();
var_dump($obj4 instanceof Child);
?>
```

Результат виконання наведеного прикладу:

```
bool(true)
bool(true)
bool(true)
```

Звернутися до властивості або методу щойно створеного об'єкта можна за допомогою одного виразу:

**Приклад #7 Доступ до властивостей/методів щойно створеного об'єкта**

```php
<?php
echo (new DateTime())->format('Y');
?>
```

Висновок наведеного прикладу буде схожим на:

```
2016
```

> **Зауваження**: До PHP 7.1 аргументи не мали значення, якщо не визначено функцію конструктора.

### Властивості та методи

Властивості та методи класу живуть у розділених "просторах імен", так що можливо мати властивість та метод з одним і тим же ім'ям. Посилання як на властивості, так і на методи мають однакову нотацію, і виходить, що отримаєте ви доступ до властивості або викличе метод - визначається контекстом використання.

**Приклад #8 Доступ до якості vs. виклик методу**

```php
<?php
class Foo
{
    public $bar = 'свойство';

    public function bar() {
        return 'метод';
    }
}

$obj = new Foo();
echo $obj->bar, PHP_EOL, $obj->bar(), PHP_EOL;
```

Результат виконання наведеного прикладу:

```
свойство
метод
```

Це означає, що викликати [анонімну функцію](functions.anonymous.md), Присвоєну змінною, безпосередньо не вийде. Натомість властивість має бути призначена, наприклад, змінною. Можна викликати таку властивість безпосередньо, уклавши її в дужки.

**Приклад #9 Виклик анонімної функції, що міститься у властивості**

```php
<?php
class Foo
{
    public $bar;

    public function __construct() {
        $this->bar = function() {
            return 42;
        };
    }
}

$obj = new Foo();

echo ($obj->bar)(), PHP_EOL;
```

Результат виконання наведеного прикладу:

```
42
```

### extends

Клас може успадковувати константи, методи та властивості іншого класу, використовуючи ключове слово `extends` у його оголошенні. Неможливо успадковувати кілька класів, один клас може успадковувати лише один базовий клас.

Наслідувані константи, методи та властивості можуть бути перевизначені (за винятком випадків, коли метод або константа класу оголошені як [final](language.oop5.final.md)) шляхом оголошення їх із тими самими іменами, як й у батьківському класі. Існує можливість доступу до перевизначених методів або статичних властивостей шляхом звернення до них через [parent::](language.oop5.paamayim-nekudotayim.md)

> **Зауваження**: Починаючи з PHP 8.1.0, константи можна оголошувати остаточними (final).

**Приклад #10 Просте спадкування класів**

```php
<?php
class ExtendClass extends SimpleClass
{
    // Переопределение метода родителя
    function displayVar()
    {
        echo "Расширенный класс\n";
        parent::displayVar();
    }
}

$extended = new ExtendClass();
$extended->displayVar();
?>
```

Результат виконання наведеного прикладу:

```
Расширенный класс
значение по умолчанию
```

#### Правила сумісності сигнатури

При перевизначенні методу його сигнатура має бути сумісною з батьківським методом. В іншому випадку видається фатальна помилка або, до PHP 8.0.0, генерується помилка рівня **`E_WARNING`**. Сигнатура є сумісною, якщо вона відповідає правилам [контраваріантності](language.oop5.variance.md), робить обов'язковий параметр необов'язковим, додає лише необов'язкові нові параметри та не обмежує, а лише послаблює видимість. Це відомо як принцип підстановки Барбари Лисків або скорочено LSP. Правила сумісності не поширюються на [конструктор](language.oop5.decon.md#language.oop5.decon.constructor)и сигнатуру`private` методів, вони не будуть видавати фатальну помилку у разі невідповідності сигнатури.

**Приклад #11 Сумісність дочірніх методів**

```php
<?php

class Base
{
    public function foo(int $a) {
        echo "Допустимо\n";
    }
}

class Extend1 extends Base
{
    function foo(int $a = 5)
    {
        parent::foo($a);
    }
}

class Extend2 extends Base
{
    function foo(int $a, $b = 5)
    {
        parent::foo($a);
    }
}

$extended1 = new Extend1();
$extended1->foo();
$extended2 = new Extend2();
$extended2->foo(1);
```

Результат виконання наведеного прикладу:

```
Допустимо
Допустимо
```

Наступні приклади демонструють, що дочірній метод, який видаляє параметр або робить необов'язковий параметр, несумісний з батьківським методом.

**Приклад #12 Фатальна помилка, коли дочірній метод видаляє параметр**

```php
<?php

class Base
{
    public function foo(int $a = 5) {
        echo "Допустимо\n";
    }
}

class Extend extends Base
{
    function foo()
    {
        parent::foo(1);
    }
}
```

Результат виконання наведеного прикладу PHP 8 аналогічний:

```
Fatal error: Declaration of Extend::foo() must be compatible with Base::foo(int $a = 5) in /in/evtlq on line 13
```

**Приклад #13 Фатальна помилка, коли дочірній метод робить необов'язковим параметром.**

```php
<?php

class Base
{
    public function foo(int $a = 5) {
        echo "Допустимо\n";
    }
}

class Extend extends Base
{
    function foo(int $a)
    {
        parent::foo($a);
    }
}
```

Результат виконання наведеного прикладу PHP 8 аналогічний:

```
Fatal error: Declaration of Extend::foo(int $a) must be compatible with Base::foo(int $a = 5) in /in/qJXVC on line 13
```

**Увага**

Перейменування параметра методу дочірньому класі перестав бути несумісністю сигнатури. Однак це не рекомендується, оскільки призведе до [Error](class.error.md) під час виконання, якщо використовуються [іменовані аргументи](functions.arguments.md#functions.named-arguments)

**Приклад #14 Помилка використання іменованих аргументів і параметрів, перейменованих у дочірньому класі**

```php
<?php

class A {
    public function test($foo, $bar) {}
}

class B extends A {
    public function test($a, $b) {}
}

$obj = new B;

// Передача параметров согласно контракту A::test()
$obj->test(foo: "foo", bar: "bar"); // ОШИБКА!
```

Висновок наведеного прикладу буде схожим на:

```
Fatal error: Uncaught Error: Unknown named parameter $foo in /in/XaaeN:14
Stack trace:
#0 {main}
  thrown in /in/XaaeN on line 14
```

### ::class

Ключевое слово`class` використовується для дозволу імені класу. Щоб отримати повне ім'я класу `ClassName`, используйте`ClassName::class`. Зазвичай це досить корисно під час роботи з класами, які використовують [простору імен](language.namespaces.md)

**Приклад #15 Дозвіл імені класу**

```php
<?php
namespace NS {
    class ClassName {
    }

    echo ClassName::class;
}
?>
```

Результат виконання наведеного прикладу:

```
NS\ClassName
```

> **Зауваження** :
> 
> Дозвіл імен класу з використанням `::class` відбувається на етапі компіляції. Це означає, що на момент створення рядка з ім'ям класу автозавантаження не відбувається. Як наслідок, імена класів розкриваються навіть якщо клас не існує. Помилка у разі не видається.
> 
> **Приклад #16 Відсутня роздільна здатність імені класу**
> 
> ```php
> <?php
> print Does\Not\Exist::class;
> ?>
> ```
> 
> Результат виконання наведеного прикладу:
> 
> ```
> Does\Not\Exist
> ```

Начиная с PHP 8.0.0, константа`::class` також може використовуватись для об'єктів. Цей дозвіл відбувається під час виконання, а чи не під час компіляції. Те саме, що і при виклику [get\_class()](function.get-class.md) для об'єкту.

**Приклад #17 Роздільна здатність імені об'єкта**

```php
<?php
namespace NS {
    class ClassName {
    }
}
$c = new ClassName();
print $c::class;
?>
```

Результат виконання наведеного прикладу:

```
NS\ClassName
```

### Методи та властивості Nullsafe

Починаючи з PHP 8.0.0, до властивостей та методів можна також звертатися за допомогою оператора "nullsafe": `?->`. Оператор nullsafe працює так само, як доступ до властивості або методу, як зазначено вище, за винятком того, що якщо розйменування об'єкта видає **`null`**, то буде повернутий **`null`**, а не викинуто виняток. Якщо розіменування є частиною ланцюжка, решта ланцюжка пропускається.

Аналогічно висновку кожного звернення до [is\_null()](function.is-null.md), але компактніший.

**Приклад #18 Оператор Nullsafe**

```php
<?php

// Начиная с PHP 8.0.0, эта строка:
$result = $repository?->getUser(5)?->name;

// Эквивалентна следующему блоку кода:
if (is_null($repository)) {
    $result = null;
} else {
    $user = $repository->getUser(5);
    if (is_null($user)) {
        $result = null;
    } else {
        $result = $user->name;
    }
}
?>
```

> **Зауваження** :
> 
> Оператор nullsafe найкраще використовувати, коли null вважається допустимим і очікуваним значенням для властивості або методу, що повертається. Для індикації помилки краще викидати виняток.
