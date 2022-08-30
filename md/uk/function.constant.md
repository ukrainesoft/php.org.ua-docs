Повертає значення константи

-   [« connectionstatus](function.connection-status.html)
    
-   [define »](function.define.md)
    
-   [PHP Manual](index.md)
    
-   [Різні функції](ref.misc.md)
    
-   Повертає значення константи
    

# constant

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

constant — Повертає значення константи

### Опис

```methodsynopsis
constant(string $name): mixed
```

Повертає значення константи, вказаної у параметрі `name`

Функція **constant()** корисна, якщо вам необхідно отримати значення константи, але невідомо її ім'я. Наприклад, якщо воно зберігається у змінній або повертається функцією.

Ця функція також працює з [константами класів](language.oop5.constants.md)

### Список параметрів

`name`

Ім'я константи.

### Значення, що повертаються

Повертає значення константи.

### Помилки

Якщо константа не визначена, викидається виняток [Error](class.error.md). До PHP 8.0.0 у цьому випадку видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Описание |
| --- | --- |
|  | Якщо константа не визначена, функція **constant()** тепер викидає виняток [Error](class.error.md); раніше видавалася помилка рівня **`E_WARNING`** і поверталося значення **`null`** |

### Приклади

**Приклад #1 Приклад функції **constant()****

```php
<?php

define("MAXSIZE", 100);

echo MAXSIZE;
echo constant("MAXSIZE"); // результат аналогичен предыдущему выводу


interface bar {
    const test = 'foobar!';
}

class foo {
    const test = 'foobar!';
}

$const = 'test';

var_dump(constant('bar::'. $const)); // string(7) "foobar!"
var_dump(constant('foo::'. $const)); // string(7) "foobar!"

?>
```

### Дивіться також

-   [define()](function.define.md) - визначає іменовану константу
-   [defined()](function.defined.md) - Перевіряє існування вказаної іменованої константи
-   [getdefinedconstants()](function.get-defined-constants.html) - Повертає асоціативний масив з іменами всіх констант та їх значень
-   Дивіться розділ [Константи](language.constants.md)