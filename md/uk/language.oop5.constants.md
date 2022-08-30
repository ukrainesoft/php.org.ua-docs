Константи класів

-   [« Свойства](language.oop5.properties.md)
    
-   [Автоматичне завантаження класів »](language.oop5.autoload.md)
    
-   [PHP Manual](index.md)
    
-   [Класи та об'єкти](language.oop5.md)
    
-   Константи класів
    

## Константи класів

[Константи](language.constants.md) також можуть бути оголошені у межах одного класу. Область видимості констант за замовчуванням `public`

> **Зауваження**
> 
> Константи класу може бути перевизначені дочірнім класом. Починаючи з PHP 8.1.0, константи класу не можуть бути перевизначені дочірнім класом, якщо він визначений як остаточний ([final](language.oop5.final.md)

Інтерфейси також можуть містити `константы`. За прикладами звертайтесь до розділу про [інтерфейсах](language.oop5.interfaces.md)

До класу можна звернутись за допомогою змінної. Значення змінної не може бути ключовим словом (наприклад, `self` `parent` і `static`

Зверніть увагу, що константи класу задаються один раз для класу, а не окремо для кожного створеного об'єкта цього класу.

**Приклад #1 Оголошення та використання константи**

```php
<?php
class MyClass
{
    const CONSTANT = 'значение константы';

    function showConstant() {
        echo  self::CONSTANT . "\n";
    }
}

echo MyClass::CONSTANT . "\n";

$classname = "MyClass";
echo $classname::CONSTANT . "\n";

$class = new MyClass();
$class->showConstant();

echo $class::CONSTANT."\n";
?>
```

Спеціальна константа **`::class`**, Якою на етапі компіляції надається повне ім'я класу, корисна при використанні з класами, що використовують простори імен.

**Приклад #2 Приклад використання ::class з простором імен**

```php
<?php
namespace foo {
    class bar {
    }

    echo bar::class; // foo\bar
}
?>
```

**Приклад #3 Приклад констант, заданих виразом**

```php
<?php
const ONE = 1;

class foo {
    const TWO = ONE * 2;
    const THREE = ONE + self::TWO;
    const SENTENCE = 'Значение константы THREE - ' . self::THREE;
}
?>
```

**Приклад #4 Модифікатори видимості констант класу, починаючи з PHP 7.1.0**

```php
<?php
class Foo {
    public const BAR = 'bar';
    private const BAZ = 'baz';
}
echo Foo::BAR, PHP_EOL;
echo Foo::BAZ, PHP_EOL;
?>
```

Результат виконання цього прикладу в PHP 7.1:

```
bar

Fatal error: Uncaught Error: Cannot access private const Foo::BAZ in …
```

> **Зауваження**
> 
> Починаючи з PHP 7.1.0, для констант класу можна використовувати модифікатори області видимості.