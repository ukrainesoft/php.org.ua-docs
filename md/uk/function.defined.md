---
navigation:
  - function.define.md: « define
  - function.die.md: die »
  - index.md: PHP Manual
  - ref.misc.md: Різні функції
title: defined
---
# defined

(PHP 4, PHP 5, PHP 7, PHP 8)

defined — Перевіряє існування вказаної константи.

### Опис

```methodsynopsis
defined(string $constant_name): bool
```

Перевіряє існування та наявність значення зазначеної константи.

> **Зауваження**
> 
> Якщо необхідно дізнатися про існування змінної, використовуйте [isset()](function.isset.md), так як **defined()** застосовна лише для [констант](language.constants.md). Якщо вам необхідно дізнатися про існування функції, використовуйте [functionexists()](function.function-exists.md)

### Список параметрів

`constant_name`

Ім'я константи.

### Значення, що повертаються

Повертає **`true`**, якщо іменована константа, зазначена у параметрі `constant_name`, була визначена, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Перевірка констант**

```php
<?php
/* Важно учесть необходимость использования кавычек. Данный пример проверяет,
 * является ли строка 'TEST' именем константы TEST. */
if (defined('TEST')) {
    echo TEST;
}
?>
```

### Дивіться також

-   [define()](function.define.md) - визначає іменовану константу
-   [constant()](function.constant.md) - Повертає значення константи
-   [getdefinedconstants()](function.get-defined-constants.md) - Повертає асоціативний масив з іменами всіх констант та їх значень
-   [functionexists()](function.function-exists.md) - Повертає true, якщо вказана функція визначена
-   Дивіться розділ [Константи](language.constants.md)
