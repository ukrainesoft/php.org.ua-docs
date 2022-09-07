---
navigation:
  - language.oop5.decon.md: « Конструктори та деструктори
  - language.oop5.inheritance.md: Наследование »
  - index.md: PHP Manual
  - language.oop5.md: Класи та об'єкти
title: Область видимості
---
## Область видимості

Область видимості властивості, методу або константи (починаючи з PHP 7.1.0) може бути визначена шляхом використання таких ключових слів у оголошенні: `public` `protected` або `private`. Доступ до властивостей та методів класу, оголошених як public (загальнодоступний), дозволено звідусіль. Модифікатор protected (захищений) дозволяє доступ самому класу, його класам і батьківським класам. Модифікатор private (закритий) обмежує область видимості так, що тільки клас, де оголошено сам елемент, має доступ до нього.

### Область видимості якості

Властивості класу можуть бути визначені як public, private або protected. Властивості, оголошені без явного ключового слова області видимості, визначаються загальнодоступними (public).

**Приклад #1 Оголошення якості класу**

```php
<?php
/**
 * Определение MyClass
 */
class MyClass
{
    public $public = 'Public';
    protected $protected = 'Protected';
    private $private = 'Private';

    function printHello()
    {
        echo $this->public;
        echo $this->protected;
        echo $this->private;
    }
}

$obj = new MyClass();
echo $obj->public; // Работает
echo $obj->protected; // Неисправимая ошибка
echo $obj->private; // Неисправимая ошибка
$obj->printHello(); // Выводит Public, Protected и Private


/**
 * Определение MyClass2
 */
class MyClass2 extends MyClass
{
    // Мы можем переопределить общедоступные и защищённые свойства, но не закрытые
    public $public = 'Public2';
    protected $protected = 'Protected2';

    function printHello()
    {
        echo $this->public;
        echo $this->protected;
        echo $this->private;
    }
}

$obj2 = new MyClass2();
echo $obj2->public; // Работает
echo $obj2->private; // Неопределён
echo $obj2->protected; // Неисправимая ошибка
$obj2->printHello(); // Выводит Public2, Protected2, Undefined

?>
```

### Область видимості методу

Методи класу можуть бути визначені як public, private або protected. Методи, оголошені без вказівки на область видимості, визначаються як public.

**Приклад #2 Оголошення методу**

```php
<?php
/**
 * Определение MyClass
 */
class MyClass
{
    // Объявление общедоступного конструктора
    public function __construct() { }

    // Объявление общедоступного метода
    public function MyPublic() { }

    // Объявление защищённого метода
    protected function MyProtected() { }

    // Объявление закрытого метода
    private function MyPrivate() { }

    // Это общедоступный метод
    function Foo()
    {
        $this->MyPublic();
        $this->MyProtected();
        $this->MyPrivate();
    }
}

$myclass = new MyClass;
$myclass->MyPublic(); // Работает
$myclass->MyProtected(); // Неисправимая ошибка
$myclass->MyPrivate(); // Неисправимая ошибка
$myclass->Foo(); // Работает общедоступный, защищённый и закрытый


/**
 * Определение MyClass2
 */
class MyClass2 extends MyClass
{
    // Это общедоступный метод
    function Foo2()
    {
        $this->MyPublic();
        $this->MyProtected();
        $this->MyPrivate(); // Неисправимая ошибка
    }
}

$myclass2 = new MyClass2;
$myclass2->MyPublic(); // Работает
$myclass2->Foo2(); // Работает общедоступный и защищённый, закрытый не работает

class Bar
{
    public function test() {
        $this->testPrivate();
        $this->testPublic();
    }

    public function testPublic() {
        echo "Bar::testPublic\n";
    }

    private function testPrivate() {
        echo "Bar::testPrivate\n";
    }
}

class Foo extends Bar
{
    public function testPublic() {
        echo "Foo::testPublic\n";
    }

    private function testPrivate() {
        echo "Foo::testPrivate\n";
    }
}

$myFoo = new Foo();
$myFoo->test(); // Bar::testPrivate
                // Foo::testPublic
?>
```

### Область видимості констант

Починаючи з PHP 7.1.0, константи класу можуть бути визначені як public, private чи protected. Константи, оголошені без зазначення області видимості, визначаються як public.

**Приклад #3 Оголошення констант, починаючи з PHP 7.1.0**

```php
<?php
/**
 * Объявление класса MyClass
 */
class MyClass
{
    // Объявление общедоступной константы
    public const MY_PUBLIC = 'public';

    // Объявление защищённой константы
    protected const MY_PROTECTED = 'protected';

    // Объявление закрытой константы
    private const MY_PRIVATE = 'private';

    public function foo()
    {
        echo self::MY_PUBLIC;
        echo self::MY_PROTECTED;
        echo self::MY_PRIVATE;
    }
}

$myclass = new MyClass();
MyClass::MY_PUBLIC; // Работает
MyClass::MY_PROTECTED; // Неисправимая ошибка
MyClass::MY_PRIVATE; // Неисправимая ошибка
$myclass->foo(); // Выводятся константы public, protected и private


/**
 * Объявление класса MyClass2
 */
class MyClass2 extends MyClass
{
    // Публичный метод
    function foo2()
    {
        echo self::MY_PUBLIC;
        echo self::MY_PROTECTED;
        echo self::MY_PRIVATE; // Неисправимая ошибка
    }
}

$myclass2 = new MyClass2;
echo MyClass2::MY_PUBLIC; // Работает
$myclass2->foo2(); // Выводятся константы public и protected, но не private
?>
```

### Видимість з інших об'єктів

Об'єкти, які мають загальний тип (успадковуються від одного класу), мають доступ до елементів з модифікаторами private і protected один одного, навіть якщо не є одним і тим самим екземпляром. Це тим, що реалізація видимості елементів відома всередині цих об'єктів.

**Приклад #4 Доступ до елементів із модифікатором private з об'єктів одного типу**

```php
<?php
class Test
{
    private $foo;

    public function __construct($foo)
    {
        $this->foo = $foo;
    }

    private function bar()
    {
        echo 'Доступ к закрытому методу.';
    }

    public function baz(Test $other)
    {
        // Мы можем изменить закрытое свойство:
        $other->foo = 'привет';
        var_dump($other->foo);

        // Мы также можем вызвать закрытый метод:
        $other->bar();
    }
}

$test = new Test('test');

$test->baz(new Test('other'));
?>
```

Результат виконання цього прикладу:

```
string(6) "привет"
Доступ к закрытому методу.
```
