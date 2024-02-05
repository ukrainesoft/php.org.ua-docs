---
navigation:
  - function.connection-status.md: « connection\_status
  - function.define.md: define »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: constant
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# constant

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

constant — Повертає значення константи

### Опис

```methodsynopsis
constant(string $name): mixed
```

Повертає значення константи, вказаної у параметрі `name`

Функция**constant()** корисна, якщо вам необхідно отримати значення константи, але невідомо її ім'я. Наприклад, якщо воно зберігається у змінній або повертається функцією.

Ця функція також працює з [константами класів](language.oop5.constants.md) і [варіантами перерахування](language.types.enumerations.md)

### Список параметрів

`name`

Ім'я константи.

### Значення, що повертаються

Повертає значення константи.

### Помилки

Якщо константа не визначена, викидається виняток [Error](class.error.md). До PHP 8.0.0 у цьому випадку видавалася помилка рівня **`E_WARNING`**

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Якщо константа не визначена, функція **constant()** тепер викидає виняток [Error](class.error.md); раніше видавалася помилка рівня **`E_WARNING`** і поверталося значення **`null`** |

### Приклади

**Пример #1 Пример использования**constant()\*\* з константами\*\*

```php
<?php

define("MAXSIZE", 100);

echo MAXSIZE;
echo constant("MAXSIZE"); // результат аналогичен предыдущему выводу


interface bar {
    const test = 'foobar!';
}

class foo {
    const test = 'foobar!';
}

$const = 'test';

var_dump(constant('bar::'. $const)); // string(7) "foobar!"
var_dump(constant('foo::'. $const)); // string(7) "foobar!"

?>
```

**Пример #2 Пример использования**constant()\*\* з варіантами перерахування (починаючи з PHP 8.1.0)\*\*

```php
<?php

enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

$case = 'Hearts';

var_dump(constant('Suit::'. $case)); // enum(Suit::Hearts)

?>
```

### Дивіться також

-   [define()](function.define.md) \- визначає іменовану константу
-   [defined()](function.defined.md) \- Перевіряє існування вказаної іменованої константи
-   [get\_defined\_constants()](function.get-defined-constants.md) \- Повертає асоціативний масив з іменами всіх констант та їх значень
-   Смотрите раздел [Константи](language.constants.md)
