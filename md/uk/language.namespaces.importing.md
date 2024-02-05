---
navigation:
  - language.namespaces.nsconstants.md: « Ключове слово namespace та константа\_\_NAMESPACE\_\_
  - language.namespaces.global.md: Глобальний простір »
  - index.md: PHP Manual
  - language.namespaces.md: Простори імен
title: 'Простори імен: псевдонімування та імпорт'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Простори імен: псевдонімування та імпорт

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

Здатність посилатися на зовнішнє абсолютне ім'я псевдоніму або імпортувати зовнішні абсолютні імена - це важлива властивість просторів імен. Це схоже на здатність файлових систем на основі Unix створювати символічні посилання на файл або директорію.

PHP вміє створювати псевдоніми або імпортувати константи, функції, класи, інтерфейси, трейти, перерахування та простори імен.

Псевдонім імені створюють, вказуючи ключове слово `use`. Ось приклад, який показує 5 типів імпорту:

**Приклад #1 Імпорт або псевдонімування через ключове слово use**

```php
<?php

namespace foo;

use My\Full\Classname as Another;

// это то же самое, что и My\Full\NSname as NSname
use My\Full\NSname;

// импортирование глобального класса
use ArrayObject;

// импортирование функции
use function My\Full\functionName;

// создание псевдонима функции
use function My\Full\functionName as func;

// импортирование константы
use const My\Full\CONSTANT;

$obj = new namespace\Another; // создаёт экземпляр класса foo\Another
$obj = new Another; // создаёт объект класса My\Full\Classname
NSname\subns\func(); // вызывает функцию My\Full\NSname\subns\func

$a = new ArrayObject(array(1)); // создаёт объект класса ArrayObject
// без выражения «use ArrayObject» был бы создан объект класса foo\ArrayObject

func(); // вызывает функцию My\Full\functionName
echo CONSTANT; // выводит содержимое константы My\Full\CONSTANT

?>
```

Зверніть увагу, що іменам усередині простору імен (абсолютним іменам просторів імен, які містять роздільник просторів імен, наприклад `Foo\Bar`, на відміну від глобальних імен, які його не містять, наприклад `FooBar`) початковий зворотний сліш (\\) не потрібен і не рекомендований, оскільки імена, що імпортуються, повинні бути абсолютними і не обробляються щодо поточного простору імен.

PHP додатково підтримує зручне скорочення для завдання кількох операторів use в одному і тому ж рядку

**Приклад #2 Імпорт або створення псевдоніма через ключове слово use, комбінування кількох виразів**

```php
<?php

use My\Full\Classname as Another, My\Full\NSname;

$obj = new Another; // создаёт объект класса My\Full\Classname
NSname\subns\func(); // вызывает функцию My\Full\NSname\subns\func

?>
```

Імпорт виконується під час компіляції, тому не впливає на імена динамічних класів, функцій або констант.

**Приклад #3 Імпорт та динамічні імена**

```php
<?php

use My\Full\Classname as Another, My\Full\NSname;

$obj = new Another; // создаёт объект класса My\Full\Classname
$a = 'Another';
$obj = new $a;      // создаёт объект класса Another

?>
```

Крім того, імпорт поширюється тільки на неповні та повні імена. На абсолютні імена операція імпорту не впливає.

**Приклад #4 Імпортування та абсолютні імена**

```php
<?php

use My\Full\Classname as Another, My\Full\NSname;

$obj = new Another; // создаёт объект класса My\Full\Classname
$obj = new \Another; // создаёт объект класса Another
$obj = new Another\thing; // создаёт объект класса My\Full\Classname\thing
$obj = new \Another\thing; // создаёт объект класса Another\thing

?>
```

### Огляд правил імпорту

Ключевое слово`use` має бути вказано на самому початку файлу (у глобальній області) або всередині оголошення простору імен. Це необхідно тому, що імпорт виконується під час компіляції, а не під час виконання, тому його не можна укладати в блок. Наступний приклад показує неприпустиму вказівку ключового слова `use` :

**Приклад #5 Неприпустиме правило імпорту**

```php
<?php

namespace Languages;

function toGreenlandic()
{
    use Languages\Danish;

    //...
}

?>
```

> **Зауваження** :
> 
> Правила імпорту задають кожен файл окремо. Тому файли, що приєднуються *НЕ*будут наследовать правила импорта из родительского файла.

### Групові оголошення через ключове слово `use`

Класи, функції та константи, що імпортуються з одного і того ж простору імен ([`namespace`](language.namespaces.definition.md)), можна групувати в одному виразі з ключовим словом [`use`](language.namespaces.importing.md)

```php
<?php

use some\namespace\ClassA;
use some\namespace\ClassB;
use some\namespace\ClassC as C;

use function some\namespace\fn_a;
use function some\namespace\fn_b;
use function some\namespace\fn_c;

use const some\namespace\ConstA;
use const some\namespace\ConstB;
use const some\namespace\ConstC;

// Эквивалентно следующему групповому объявлению с ключевым словом use
use some\namespace\{ClassA, ClassB, ClassC as C};
use function some\namespace\{fn_a, fn_b, fn_c};
use const some\namespace\{ConstA, ConstB, ConstC};
```
