---
navigation:
  - functions.returning-values.md: « Возврат значений
  - functions.internal.md: Вбудовані функції »
  - index.md: PHP Manual
  - language.functions.md: Функції
title: Звернення до функцій через змінні
---
## Звернення до функцій через змінні

PHP підтримує концепцію змінних функцій. Це означає, що якщо до імені змінної приєднані круглі дужки, PHP шукає функцію з тим самим ім'ям, що й результат обчислення змінної, і намагається її виконати. Цю можливість можна використовувати для реалізації зворотних викликів, таблиць функцій та безлічі інших речей.

Змінні функції не працюватимуть з такими мовними конструкціями, як [echo](function.echo.md) [print](function.print.md) [unset()](function.unset.md) [isset()](function.isset.md) [empty()](function.empty.md) [include](function.include.md) [require](function.require.md) і т.п. Вам необхідно реалізувати свою функцію-обертку для того, щоб наведені вище конструкції могли працювати зі змінними функціями.

**Приклад #1 Робота з функціями за допомогою змінних**

```php
<?php
function foo() {
    echo "В foo()<br />\n";
}

function bar($arg = '')
{
    echo "В bar(); аргумент был '$arg'.<br />\n";
}

// Функция-обёртка для echo
function echoit($string)
{
    echo $string;
}

$func = 'foo';
$func();        // Вызывает функцию foo()

$func = 'bar';
$func('test');  // Вызывает функцию bar()

$func = 'echoit';
$func('test');  // Вызывает функцию echoit()
?>
```

Ви також можете викликати методи об'єкта, використовуючи можливості PHP для роботи зі змінними функціями.

**Приклад #2 Звернення до методів класу за допомогою змінних**

```php
<?php
class Foo
{
    function Variable()
    {
        $name = 'Bar';
        $this->$name(); // Вызываем метод Bar()
    }

    function Bar()
    {
        echo "Это Bar";
    }
}

$foo = new Foo();
$funcname = "Variable";
$foo->$funcname();  // Обращаемся к $foo->Variable()

?>
```

При виклику статичних методів виклик функції "сильніший", ніж оператор доступу до статичної властивості:

**Приклад #3 Приклад виклику змінного методу зі статичною властивістю**

```php
<?php
class Foo
{
    static $variable = 'статическое свойство';
    static function Variable()
    {
        echo 'Вызов метода Variable';
    }
}

echo Foo::$variable; // Это выведет 'статическое свойство'. Переменная $variable будет разрешена в этой области видимости.
$variable = "Variable";
Foo::$variable();  // Это вызовет $foo->Variable(), прочитав $variable из этой области видимости.

?>
```

**Приклад #4 Складні callable функції**

```php
<?php
class Foo
{
    static function bar()
    {
        echo "bar\n";
    }
    function baz()
    {
        echo "baz\n";
    }
}

$func = array("Foo", "bar");
$func(); // выведет "bar"
$func = array(new Foo, "baz");
$func(); // выведет "baz"
$func = "Foo::bar";
$func(); // выведет "bar"
?>
```

### Дивіться також

-   [ісcallable()](function.is-callable.md)
-   [calluserfunc()](function.call-user-func.md)
-   [functionexists()](function.function-exists.md)
-   [змінні змінних](language.variables.variable.md)
