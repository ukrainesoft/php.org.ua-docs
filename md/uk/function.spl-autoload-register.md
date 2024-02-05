---
navigation:
  - function.spl-autoload-functions.md: « spl\_autoload\_functions
  - function.spl-autoload-unregister.md: spl\_autoload\_unregister »
  - index.md: PHP Manual
  - ref.spl.md: Функції SPL
title: spl\_autoload\_register
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# spl\_autoload\_register

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

spl\_autoload\_register - Реєструє задану функцію як реалізацію методу \_\_autoload()

### Опис

```methodsynopsis
spl_autoload_register(?callable $callback = null, bool $throw = true, bool $prepend = false): bool
```

Реєструє функцію \_\_autoload у наданій SPL черзі. В результаті чергу буде активовано, навіть якщо раніше її було вимкнено.

Если в вашем скрипте реализована функция[\_\_autoload()](function.autoload.md), її необхідно явно зареєструвати у черзі \_\_autoload. Це потрібно, т.к . \*\*spl\_autoload\_register()\*\*полностью заменяет механизм кеширования[\_\_autoload()](function.autoload.md)функциями[spl\_autoload()](function.spl-autoload.md) і [spl\_autoload\_call()](function.spl-autoload-call.md)

**spl\_autoload\_register()** дозволяє задати кілька реалізацій методу автозавантаження. Вона створює чергу з функцій автозавантаження як їх визначення у скрипті, тоді як вбудована функція [\_\_autoload()](function.autoload.md) може мати лише одну реалізацію.

### Список параметрів

`callback`

Имя функции, реализующей метод[spl\_autoload()](function.spl-autoload.md). Якщо **`null`**, буде зареєстровано реалізацію за замовчуванням.

```methodsynopsis
callback(string $class): void
```

`throw`

Цей параметр визначає, чи має **spl\_autoload\_register()** викидати виняток, якщо зареєструвати `callback` виявилося неможливим.

**Увага**

Починаючи з PHP 8.0.0, цей параметр ігнорується, а при установці значення **`false`** буде видано повідомлення. Функція **spl\_autoload\_register()** тепер завжди викидатиме виняток [TypeError](class.typeerror.md) у разі передачі некоректних аргументів.

`prepend`

Якщо передано значення true, \*\*spl\_autoload\_register()\*\*поместит указанную функцию в начало очереди вместо добавления в конец.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | `callback` тепер допускає значення null. |

### Приклади

**Приклад #1**spl\_autoload\_register()\*\* як альтернатива функції [\_\_autoload()](function.autoload.md)\*\*

```php
<?php

// function __autoload($class) {
//     include 'classes/' . $class . '.class.php';
// }

function my_autoloader($class) {
    include 'classes/' . $class . '.class.php';
}

spl_autoload_register('my_autoloader');

// Можно использовать анонимные функции
spl_autoload_register(function ($class) {
    include 'classes/' . $class . '.class.php';
});

?>
```

**Приклад #2 Приклад використання** spl\_autoload\_register()\*\* у випадку, якщо клас не завантажився\*\*

```php
<?php

namespace Foobar;

class Foo {
    static public function test($class) {
        print '[['. $class .']]';
    }
}

spl_autoload_register(__NAMESPACE__ .'\Foo::test');

new InexistentClass;

?>
```

Висновок наведеного прикладу буде схожим на:

```
[[Foobar\InexistentClass]]
Fatal error: Class 'Foobar\InexistentClass' not found in ...
```

**Приклад #3 Ідентифікатор буде надано без провідного зворотного сліша**

```php
<?php

spl_autoload_register(static function ($class) {
    var_dump($class);
});

class_exists('RelativeName');
class_exists('RelativeName\\WithNamespace');
class_exists('\\AbsoluteName');
class_exists('\\AbsoluteName\\WithNamespace');

?>
```

Результат виконання наведеного прикладу:

```
string(12) "RelativeName"
string(26) "RelativeName\WithNamespace"
string(12) "AbsoluteName"
string(26) "AbsoluteName\WithNamespace"
```

### Дивіться також

-   [\_\_autoload()](function.autoload.md) \- Спроба завантажити невизначений клас
