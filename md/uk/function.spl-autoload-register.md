---
navigation:
  - function.spl-autoload-functions.md: « splautoloadfunctions
  - function.spl-autoload-unregister.md: splautoloadunregister »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: splautoloadregister
---
# splautoloadregister

(PHP 5> = 5.1.0, PHP 7, PHP 8)

splautoloadregister - Реєструє задану функцію як реалізацію методу autoload()

### Опис

```methodsynopsis
spl_autoload_register(?callable $callback = null, bool $throw = true, bool $prepend = false): bool
```

Реєструє функцію autoload у наданій SPL черзі. В результаті чергу буде активовано, навіть якщо раніше її було вимкнено.

Якщо у вашому скрипті реалізовано функцію [autoload()](function.autoload.md), її необхідно явно зареєструвати у черзі autoload. Це потрібно, т.к . **splautoloadregister()** повністю замінює механізм кешування [autoload()](function.autoload.md) функціями [splautoload()](function.spl-autoload.md) і [splautoloadcall()](function.spl-autoload-call.md)

**splautoloadregister()** дозволяє задати кілька реалізацій методу автозавантаження. Вона створює чергу з функцій автозавантаження як їх визначення у скрипті, тоді як вбудована функція [autoload()](function.autoload.md) може мати лише одну реалізацію.

### Список параметрів

`callback`

Ім'я функції, що реалізує метод [splautoload()](function.spl-autoload.md). Якщо **`null`**, буде зареєстровано реалізацію за замовчуванням.

```methodsynopsis
callback(string $class_name): void
```

`throw`

Цей параметр визначає, чи має **splautoloadregister()** викидати виняток, якщо зареєструвати `callback` виявилося неможливим.

`prepend`

Якщо передано значення true, **splautoloadregister()** помістить зазначену функцію на початок черги замість додавання до кінця.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
|  | `callback` тепер допускає значення null. |

### Приклади

**Приклад #1 **splautoloadregister()** як альтернатива функції [autoload()](function.autoload.md)**

```php
<?php

// function __autoload($class) {
//     include 'classes/' . $class . '.class.php';
// }

function my_autoloader($class) {
    include 'classes/' . $class . '.class.php';
}

spl_autoload_register('my_autoloader');

// Можно использовать анонимные функции
spl_autoload_register(function ($class) {
    include 'classes/' . $class . '.class.php';
});

?>
```

**Приклад #2 Приклад використання **splautoloadregister()** у випадку, якщо клас не завантажився**

```php
<?php

namespace Foobar;

class Foo {
    static public function test($name) {
        print '[['. $name .']]';
    }
}

spl_autoload_register(__NAMESPACE__ .'\Foo::test');

new InexistentClass;

?>
```

Результатом виконання цього прикладу буде щось подібне:

```
[[Foobar\InexistentClass]]
Fatal error: Class 'Foobar\InexistentClass' not found in ...
```

### Дивіться також

-   [autoload()](function.autoload.md) - Спроба завантажити невизначений клас
