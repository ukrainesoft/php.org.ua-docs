---
navigation:
  - language.namespaces.dynamic.md: « Простори імен та динамічні особливості мови
  - language.namespaces.importing.md: 'Использование пространств имён: импорт/создание псевдонима имени »'
  - index.md: PHP Manual
  - language.namespaces.md: Пространства имён
title: Ключове слово namespace та константа NAMESPACE
---
## Ключове слово namespace та константа NAMESPACE

(PHP 5> = 5.3.0, PHP 7, PHP 8)

PHP підтримує два способи доступу до абстрактних елементів у поточному просторі імен, таких як магічна константа **`__NAMESPACE__`** та ключове слово `namespace`

Значення константи **`__NAMESPACE__`** - Це рядок, який містить ім'я поточного простору імен. У глобальному просторі поза межами імен вона містить порожній рядок.

**Приклад #1 Приклад використання константи NAMESPACE у коді з простором імен**

```php
<?php
namespace MyProject;

echo '"', __NAMESPACE__, '"'; // выводит "MyProject"
?>
```

**Приклад #2 Приклад використання константи NAMESPACE у глобальному просторі**

```php
<?php

echo '"', __NAMESPACE__, '"'; // выводит ""
?>
```

Константа **`__NAMESPACE__`** корисна для динамічно конструйованих імен, наприклад:

**Приклад #3 використання константи NAMESPACE для динамічного конструювання імені**

```php
<?php
namespace MyProject;

function get($classname)
{
    $a = __NAMESPACE__ . '\\' . $classname;
    return new $a;
}
?>
```

Ключове слово `namespace` може бути використаний для явного запиту елемента з поточного простору імен або з підпростору. Це еквівалент оператора `self` для класів у просторі імен.

**Приклад #4 Оператор namespace, всередині простору імен**

```php
<?php
namespace MyProject;

use blah\blah as mine; // смотрите "Использование пространств имён: импорт/создание псевдонима имени"

blah\mine(); // вызывает функцию MyProject\blah\mine()
namespace\blah\mine(); // вызывает функцию MyProject\blah\mine()

namespace\func(); // вызывает функцию MyProject\func()
namespace\sub\func(); // вызывает функцию MyProject\sub\func()
namespace\cname::method(); // вызывает статический метод "method" класса MyProject\cname
$a = new namespace\sub\cname(); // Создаёт экземпляр класса MyProject\sub\cname
$b = namespace\CONSTANT; // присваивает значение константы MyProject\CONSTANT переменной $b
?>
```

**Приклад #5 Оператор namespace у глобальному коді**

```php
<?php

namespace\func(); // вызывает функцию func()
namespace\sub\func(); // вызывает функцию sub\func()
namespace\cname::method(); // вызывает статический метод "method" класса cname
$a = new namespace\sub\cname(); // Создаёт экземпляр класса sub\cname
$b = namespace\CONSTANT; // присваивает значение константы CONSTANT переменной $b
?>
```
