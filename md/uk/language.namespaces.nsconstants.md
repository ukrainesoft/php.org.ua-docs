---
navigation:
  - language.namespaces.dynamic.md: « Простори імен та динамічні особливості мови
  - language.namespaces.importing.md: Псевдонімування та імпорт »
  - index.md: PHP Manual
  - language.namespaces.md: Простори імен
title: Ключове слово namespace та магічна константа \_\_NAMESPACE\_\_
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
## Ключове слово namespace та магічна константа \_\_NAMESPACE\_\_

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

PHP підтримує два способи абстрактного доступу до елементів у поточному просторі імен: магічна константа \*\*`__NAMESPACE__`\*\*и ключевое слово`namespace`

Значення константи **`__NAMESPACE__`** - Це рядок, який містить ім'я поточного простору імен. У глобальному просторі поза межами імен вона містить порожній рядок.

**Приклад #1 Приклад використання константи \_\_NAMESPACE\_\_ у коді з простором імен**

```php
<?php

namespace MyProject;

echo '"', __NAMESPACE__, '"'; // выводит «MyProject»

?>
```

**Приклад #2 Приклад використання константи \_\_NAMESPACE\_\_ у глобальному просторі**

```php
<?php

echo '"', __NAMESPACE__, '"'; // выводит ""
?>
```

Константа\*\*`__NAMESPACE__`\*\* корисна для динамічно конструйованих імен, наприклад:

**Приклад #3 Використання константи \_\_NAMESPACE\_\_ для динамічного конструювання імені**

```php
<?php

namespace MyProject;

function get($classname)
{
    $a = __NAMESPACE__ . '\\' . $classname;
    return new $a;
}

?>
```

Ключевое слово`namespace` дозволено вказувати для явного запиту елемента з поточного простору імен або підпростору. Це еквівалент ключового слова `self` для класів у просторі імен.

**Приклад #4 Ключове слово namespace всередині простору імен**

```php
<?php

namespace MyProject;

use blah\blah as mine; // смотрите «Пространства имён: псевдонимирование и импорт»

blah\mine(); // вызывает функцию MyProject\blah\mine()
namespace\blah\mine(); // вызывает функцию MyProject\blah\mine()

namespace\func(); // вызывает функцию MyProject\func()
namespace\sub\func(); // вызывает функцию MyProject\sub\func()
namespace\cname::method(); // вызывает статический метод "method" класса MyProject\cname
$a = new namespace\sub\cname(); // Создаёт экземпляр класса MyProject\sub\cname
$b = namespace\CONSTANT; // присваивает значение константы MyProject\CONSTANT переменной $b

?>
```

**Приклад #5 Ключове слово namespace у глобальному коді**

```php
<?php

namespace\func(); // Вызывает функцию func()
namespace\sub\func(); // Вызывает функцию sub\func()
namespace\cname::method(); // Вызывает статический метод «method» класса cname
$a = new namespace\sub\cname(); // Создаёт экземпляр класса sub\cname
$b = namespace\CONSTANT; // Присваивает значение константы CONSTANT переменной $b

?>
```
