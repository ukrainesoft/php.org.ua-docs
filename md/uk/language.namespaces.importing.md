Використання просторів імен: імпорт/створення псевдоніма імені

-   [« Ключевое слово namespace и константаNAMESPACE](language.namespaces.nsconstants.md)
    
-   [Глобальний простір »](language.namespaces.global.md)
    
-   [PHP Manual](index.md)
    
-   [Пространства имён](language.namespaces.md)
    
-   Використання просторів імен: імпорт/створення псевдоніма імені
    

## Використання просторів імен: імпорт/створення псевдоніма імені

(PHP 5> = 5.3.0, PHP 7, PHP 8)

Можливість посилатися на зовнішнє абсолютне ім'я щодо псевдоніму чи імпортування – це важлива особливість просторів імен. Це схоже на можливість файлових систем unix створювати символічні посилання на файл або директорію.

PHP може створювати псевдоніми імені/імпортувати константи, функції, класи, інтерфейси, трейти, перерахування та простори імен.

Створення псевдоніма імені виконується за допомогою оператора `use`. Ось приклад, що показує 5 типів імпорту:

**Приклад #1 імпорт/створення псевдоніма імені за допомогою оператора use**

```php
<?php
namespace foo;
use My\Full\Classname as Another;

// это тоже самое, что и использование My\Full\NSname as NSname
use My\Full\NSname;

// импортирование глобального класса
use ArrayObject;

// импортирование функции
use function My\Full\functionName;

// псевдоним функции
use function My\Full\functionName as func;

// импортирование константы
use const My\Full\CONSTANT;

$obj = new namespace\Another; // создаёт экземпляр класса foo\Another
$obj = new Another; // создаёт объект класса My\Full\Classname
NSname\subns\func(); // вызывает функцию My\Full\NSname\subns\func
$a = new ArrayObject(array(1)); // создаёт объект класса ArrayObject
// без выражения "use ArrayObject" мы создадим объект класса foo\ArrayObject
func(); // вызывает функцию My\Full\functionName
echo CONSTANT; // выводит содержимое константы My\Full\CONSTANT
?>
```

Зверніть увагу, що для імен у просторі імен (абсолютні імена, що містять роздільники просторів імен, такі як `Foo\Bar`, на відміну від глобальних імен, які не містять, такі як `FooBar`) немає необхідності в початковому зворотному сліші () та його присутність там не рекомендується, оскільки імпортовані імена повинні бути абсолютними та не обробляються щодо поточного простору імен.

PHP додатково підтримує зручне скорочення для завдання кількох операторів use в одному і тому ж рядку

**Приклад #2 імпорт/створення псевдоніма імені за допомогою оператора use, комбінування кількох операторів use**

```php
<?php
use My\Full\Classname as Another, My\Full\NSname;

$obj = new Another; // создаёт объект класса My\Full\Classname
NSname\subns\func(); // вызывает функцию My\Full\NSname\subns\func
?>
```

Імпорт виконується під час компіляції і тому не впливає на імена динамічних класів, функцій чи констант.

**Приклад #3 Імпорт та динамічні імена**

```php
<?php
use My\Full\Classname as Another, My\Full\NSname;

$obj = new Another; // создаёт объект класса My\Full\Classname
$a = 'Another';
$obj = new $a;      // создаёт объект класса Another
?>
```

Крім того, імпорт поширюється лише на неповні та повні імена. Абсолютні імена не торкаються операції імпорту.

**Приклад #4 Імпортування та абсолютні імена**

```php
<?php
use My\Full\Classname as Another, My\Full\NSname;

$obj = new Another; // создаёт объект класса My\Full\Classname
$obj = new \Another; // создаёт объект класса Another
$obj = new Another\thing; // создаёт объект класса My\Full\Classname\thing
$obj = new \Another\thing; // создаёт объект класса Another\thing
?>
```

### Огляд правил імпорту

Ключове слово `use` має бути вказано на самому початку файлу (у глобальній області) або всередині оголошення простору імен. Це необхідно тому, що імпорт виконується під час компіляції, а не під час виконання, тому його не можна укладати в блок. Наступний приклад показує неприпустиме застосування ключового слова `use`

**Приклад #5 Неприпустиме правило імпорту**

```php
<?php
namespace Languages;

function toGreenlandic()
{
    use Languages\Danish;

    //...
}
?>
```

> **Зауваження**
> 
> Правила імпорту задаються для кожного файлу окремо. Це означає, що файли, що приєднуються *НЕ* успадкуватимуть правила імпорту з батьківського файлу.

### Опис групування в одному операторі `use`

Класи, функції та константи, що імпортуються з одного і того ж [`namespace`](language.namespaces.definition.md), можуть групуватися в одному операторі [`use`](language.namespaces.importing.md)

```php
<?php

use some\namespace\ClassA;
use some\namespace\ClassB;
use some\namespace\ClassC as C;

use function some\namespace\fn_a;
use function some\namespace\fn_b;
use function some\namespace\fn_c;

use const some\namespace\ConstA;
use const some\namespace\ConstB;
use const some\namespace\ConstC;

// Эквивалентно следующему групповому использованию
use some\namespace\{ClassA, ClassB, ClassC as C};
use function some\namespace\{fn_a, fn_b, fn_c};
use const some\namespace\{ConstA, ConstB, ConstC};
```