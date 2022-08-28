Ключове слово static

-   [« Оператор разрешения области видимости (::)](language.oop5.paamayim-nekudotayim.html)
    
-   [Абстрактные классы »](language.oop5.abstract.html)
    
-   [PHP Manual](index.html)
    
-   [Классы и объекты](language.oop5.html)
    
-   Ключове слово static
    

## Ключове слово static

**Підказка**

Ця сторінка описує використання ключового слова `static` для визначення статичних методів та властивостей . `static` також може використовуватися для [определения статических переменных](language.variables.scope.html#language.variables.scope.static) і [позднего статического связывания](language.oop5.late-static-bindings.html). Для отримання інформації про таке застосування ключового слова `static` зверніться до вищевказаних сторінок.

Оголошення властивостей і методів статичними класу дозволяє звертатися до них без створення екземпляра класу. До них також можна отримати статичний доступ у створеному екземплярі об'єкта класу.

### Статичні методи

Так як статичні методи викликаються без створення екземпляра класу, то псевдозмінна $this недоступна всередині статичних методів.

**Увага**

Виклик нестатичних методів статично викликає помилку [Error](class.error.html)

До PHP 8.0.0 виклик нестатичних методів статично був оголошений застарілим та викликав помилку рівня **`E_DEPRECATED`**

**Приклад #1 Приклад статичного методу**

```php
<?php
class Foo {
    public static function aStaticMethod() {
        // ...
    }
}

Foo::aStaticMethod();
$classname = 'Foo';
$classname::aStaticMethod();
?>
```

### Статичні властивості

Доступ до статичних властивостей здійснюється за допомогою [оператора разрешения области видимости](language.oop5.paamayim-nekudotayim.html) `::`), і до них не можна отримати доступ через оператор об'єкта (`->`

На клас можна посилатися за допомогою змінної. Значення змінної у такому разі не може бути ключовим словом (наприклад, `self` `parent` і `static`

**Приклад #2 Приклад статичної властивості**

```php
<?php
class Foo
{
    public static $my_static = 'foo';

    public function staticValue() {
        return self::$my_static;
    }
}

class Bar extends Foo
{
    public function fooStatic() {
        return parent::$my_static;
    }
}


print Foo::$my_static . "\n";

$foo = new Foo();
print $foo->staticValue() . "\n";
print $foo->my_static . "\n";      // Не определено свойство my_static

print $foo::$my_static . "\n";
$classname = 'Foo';
print $classname::$my_static . "\n";

print Bar::$my_static . "\n";
$bar = new Bar();
print $bar->fooStatic() . "\n";
?>
```

Результат виконання цього прикладу в PHP 8 аналогічний:

```
foo
foo

Notice: Accessing static property Foo::$my_static as non static in /in/V0Rvv on line 23

Warning: Undefined property: Foo::$my_static in /in/V0Rvv on line 23

foo
foo
foo
foo
```