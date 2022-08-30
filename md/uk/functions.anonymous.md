Анонімні функції

-   [« Вбудовані функції](functions.internal.md)
    
-   [Стрілкові функції »](functions.arrow.md)
    
-   [PHP Manual](index.md)
    
-   [Функції](language.functions.md)
    
-   Анонімні функції
    

## Анонімні функції

Анонімні функції, також відомі як замикання (`closures`), дозволяють створювати функції, що не мають певних імен. Вони найбільш корисні як значення [callable](language.types.callable.md)параметрів, але також можуть мати безліч інших застосувань.

Анонімні функції реалізуються з використанням класу [](class.closure.md)[Closure](class.closure.md)

**Приклад #1 Приклад анонімної функції**

```php
<?php
echo preg_replace_callback('~-([a-z])~', function ($match) {
    return strtoupper($match[1]);
}, 'hello-world');
// выведет helloWorld
?>
```

Замикання також можуть бути використані як значення змінних; PHP автоматично перетворює такі вирази на екземпляри внутрішнього класу [Closure](class.closure.md). Присвоєння замикання змінної використовує той самий синтаксис, що і для будь-якого іншого присвоєння, включаючи точку з комою:

**Приклад #2 Приклад присвоєння анонімної функції змінної**

```php
<?php
$greet = function($name)
{
    printf("Привет, %s\r\n", $name);
};

$greet('Мир');
$greet('PHP');
?>
```

Замикання можуть успадковувати змінні з батьківської області видимості. Будь-яка подібна змінна має бути оголошена в конструкції `use`. Починаючи з PHP 7.1, ці змінні не повинні включати [superglobals](language.variables.predefined.md), $this і змінні з тими самими іменами, як і параметри функції. Оголошення типу значення функції, що повертається, повинно бути поміщене *після* конструкції `use`

**Приклад #3 Спадкування змінних із батьківської області видимості**

```php
<?php
$message = 'привет';

// Без "use"
$example = function () {
    var_dump($message);
};
$example();

// Наследуем $message
$example = function () use ($message) {
    var_dump($message);
};
$example();

// Значение унаследованной переменной задано там, где функция определена,
// но не там, где вызвана
$message = 'мир';
$example();

// Сбросим message
$message = 'привет';

// Наследование по ссылке
$example = function () use (&$message) {
    var_dump($message);
};
$example();

// Изменённое в родительской области видимости значение
// остаётся тем же внутри вызова функции
$message = 'мир';
echo $example();

// Замыкания могут принимать обычные аргументы
$example = function ($arg) use ($message) {
    var_dump($arg . ', ' . $message);
};
$example("привет");

// Объявление типа возвращаемого значения идет после конструкции use
$example = function () use ($message): string {
    return "привет $message";
};
var_dump($example());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
Notice: Undefined variable: message in /example.php on line 6
NULL
string(5) "привет"
string(5) "привет"
string(5) "привет"
string(5) "мир"
string(11) "привет мир"
string(11) "привет мир"
```

Починаючи з PHP 8.0.0, список успадкованих змінних може завершуватися комою, яка буде проігнорована.

Спадкування змінних із батьківської області видимості *не* те саме, що використання глобальних змінних. Глобальні змінні існують у глобальній області видимості, яка змінюється, незалежно від цього, яка функція виконується в даний момент. Батьківська область видимості - це функція, в якій було оголошено замикання (не обов'язково та сама, з якої воно було викликане). Дивіться наступний приклад:

**Приклад #4 Замикання та область видимості**

```php
<?php
// Базовая корзина покупок, содержащая список добавленных
// продуктов и количество каждого продукта. Включает метод,
// вычисляющий общую цену элементов корзины с помощью
// callback-замыкания.
class Cart
{
    const PRICE_BUTTER  = 1.00;
    const PRICE_MILK    = 3.00;
    const PRICE_EGGS    = 6.95;

    protected $products = array();

    public function add($product, $quantity)
    {
        $this->products[$product] = $quantity;
    }

    public function getQuantity($product)
    {
        return isset($this->products[$product]) ? $this->products[$product] :
               FALSE;
    }

    public function getTotal($tax)
    {
        $total = 0.00;

        $callback =
            function ($quantity, $product) use ($tax, &$total)
            {
                $pricePerItem = constant(__CLASS__ . "::PRICE_" .
                    strtoupper($product));
                $total += ($pricePerItem * $quantity) * ($tax + 1.0);
            };

        array_walk($this->products, $callback);
        return round($total, 2);
    }
}

$my_cart = new Cart;

// Добавляем несколько элементов в корзину
$my_cart->add('butter', 1);
$my_cart->add('milk', 3);
$my_cart->add('eggs', 6);

// Выводим общую сумму с 5% налогом на продажу.
print $my_cart->getTotal(0.05) . "\n";
// Результатом будет 54.29
?>
```

**Приклад #5 Автоматичне зв'язування `$this`**

```php
<?php

class Test
{
    public function testing()
    {
        return function() {
            var_dump($this);
        };
    }
}

$object = new Test;
$function = $object->testing();
$function();

?>
```

Результат виконання цього прикладу:

```
object(Test)#1 (0) {
}
```

При оголошенні в контексті класу, поточний клас буде автоматично пов'язаний з ним, роблячи `$this` доступним усередині функцій класу. Якщо ви не бажаєте автоматичного зв'язування з поточним класом, використовуйте [статичні анонімні функції](functions.anonymous.html#functions.anonymous-functions.static)

### Статичні анонімні функції

Анонімні функції можуть бути оголошені статично. Це запобігатиме їхньому автоматичному зв'язуванню з поточним класом. Об'єкти також не будуть пов'язані з ними під час виконання.

**Приклад #6 Спроба використовувати `$this` у статичній анонімній функції**

```php
<?php

class Foo
{
    function __construct()
    {
        $func = static function() {
            var_dump($this);
        };
        $func();
    }
};
new Foo();

?>
```

Результат виконання цього прикладу:

```
Notice: Undefined variable: this in %s on line %d
NULL
```

**Приклад #7 Спроба зв'язати об'єкт із статичною анонімною функцією**

```php
<?php

$func = static function() {
    // тело функции
};
$func = $func->bindTo(new StdClass);
$func();

?>
```

Результат виконання цього прикладу:

```
Warning: Cannot bind an instance to a static closure in %s on line %d
```

### список змін

| Версия | Описание |
| --- | --- |
|  | Анонімні функції не можуть замикатися довкола [superglobals](language.variables.predefined.md), $this або будь-яка змінна з тим же ім'ям, що і параметр. |

### Примітки

> **Зауваження**: Спільно із замиканнями можна використовувати функції [funcnumargs()](function.func-num-args.html) [funcgetarg()](function.func-get-arg.html) і [funcgetargs()](function.func-get-args.html)