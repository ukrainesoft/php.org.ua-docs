Перевіряє існування вказаної іменованої константи

-   [« define](function.define.html)
    
-   [die »](function.die.html)
    
-   [PHP Manual](index.html)
    
-   [Різні функції](ref.misc.html)
    
-   Перевіряє існування вказаної іменованої константи
    

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
> Якщо необхідно дізнатися про існування змінної, використовуйте [isset()](function.isset.html), так як **defined()** застосовна лише для [констант](language.constants.html). Якщо вам необхідно дізнатися про існування функції, використовуйте [functionexists()](function.function-exists.html)

### Список параметрів

`constant_name`

Ім'я константи.

### Значення, що повертаються

Повертає **`true`**, якщо іменована константа, зазначена у параметрі `constant_name`, була визначена, **`false`** в іншому випадку.

### Приклади

**Приклад #1 Перевірка констант**

```php
<?php
/* Важно учесть необходимость использования кавычек. Данный пример проверяет,
 * является ли строка 'TEST' именем константы TEST. */
if (defined('TEST')) {
    echo TEST;
}
?>
```

### Дивіться також

-   [define()](function.define.html) - визначає іменовану константу
-   [constant()](function.constant.html) - Повертає значення константи
-   [getdefinedconstants()](function.get-defined-constants.html) - Повертає асоціативний масив з іменами всіх констант та їх значень
-   [functionexists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
-   Дивіться розділ [Константи](language.constants.html)