---
navigation:
  - function.define.md: « define
  - function.die.md: die »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: defined
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# defined

(PHP 4, PHP 5, PHP 7, PHP 8)

defined — Перевіряє існування вказаної константи.

### Опис

```methodsynopsis
defined(string $constant_name): bool
```

Перевіряє існування та наявність значення зазначеної константи.

Функція також працює з [константами класів](language.oop5.constants.md) і [переліками](language.types.enumerations.md)

> **Зауваження** :
> 
> Якщо необхідно дізнатися про існування змінної, використовуйте [isset()](function.isset.md), так как\*\*defined()\*\*применима лишь для[констант](language.constants.md). Якщо вам необхідно дізнатися про існування функції, використовуйте [function\_exists()](function.function-exists.md)

### Список параметрів

`constant_name`

Ім'я константи.

### Значення, що повертаються

Повертає **`true`**, если именованная константа, указанная в параметре`constant_name`, була визначена, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Перевірка констант**

```php
<?php
/* Важно учесть необходимость использования кавычек. Данный пример проверяет,
 * является ли строка 'TEST' именем константы TEST. */
if (defined('TEST')) {
    echo TEST;
}

interface bar {
    const test = 'foobar!';
}

class foo {
    const test = 'foobar!';
}

var_dump(defined('bar::test')); // bool(true)
var_dump(defined('foo::test')); // bool(true)

?>
```

**Приклад #2 Перевірка варіантів перерахування (починаючи з PHP 8.1.0)**

```php
<?php

enum Suit
{
    case Hearts;
    case Diamonds;
    case Clubs;
    case Spades;
}

var_dump(defined('Suit::Hearts')); // bool(true)

?>
```

### Дивіться також

-   [define()](function.define.md) \- визначає іменовану константу
-   [constant()](function.constant.md) \- Повертає значення константи
-   [get\_defined\_constants()](function.get-defined-constants.md) \- Повертає асоціативний масив з іменами всіх констант та їх значень
-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
-   Смотрите раздел [Константи](language.constants.md)
