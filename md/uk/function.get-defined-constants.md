---
navigation:
  - function.get-current-user.md: « get\_current\_user
  - function.get-extension-funcs.md: get\_extension\_funcs »
  - index.md: PHP Manual
  - ref.info.md: Опції PHP/інформаційні функції
title: get\_defined\_constants
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_defined\_constants

(PHP 4 >= 4.1.0, PHP 5, PHP 7, PHP 8)

get\_defined\_constants - Повертає асоціативний масив з іменами всіх констант та їх значень

### Опис

```methodsynopsis
get_defined_constants(bool $categorize = false): array
```

Повертає асоціативний масив з іменами та значеннями всіх визначених нині констант. Масив буде включати константи, визначені модулями, а також створені функцією [define()](function.define.md)

### Список параметрів

`categorize`

Використання цього аргументу дає можливість отримати багатовимірний масив, у якому першому вимірі будуть міститися категорії констант, тоді як у другому відповідні імена і значення.

```php
<?php
define("MY_CONSTANT", 1);
print_r(get_defined_constants(true));
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [Core] => Array
        (
            [E_ERROR] => 1
            [E_WARNING] => 2
            [E_PARSE] => 4
            [E_NOTICE] => 8
            [E_CORE_ERROR] => 16
            [E_CORE_WARNING] => 32
            [E_COMPILE_ERROR] => 64
            [E_COMPILE_WARNING] => 128
            [E_USER_ERROR] => 256
            [E_USER_WARNING] => 512
            [E_USER_NOTICE] => 1024
            [E_ALL] => 2047
            [TRUE] => 1
        )

    [pcre] => Array
        (
            [PREG_PATTERN_ORDER] => 1
            [PREG_SET_ORDER] => 2
            [PREG_OFFSET_CAPTURE] => 256
            [PREG_SPLIT_NO_EMPTY] => 1
            [PREG_SPLIT_DELIM_CAPTURE] => 2
            [PREG_SPLIT_OFFSET_CAPTURE] => 4
            [PREG_GREP_INVERT] => 1
        )

    [user] => Array
        (
            [MY_CONSTANT] => 1
        )

)
```

### Значення, що повертаються

Повертає масив виду "ім'я константи" => "значення константи", з можливістю згрупувати його на ім'я модуля, який зареєстрував константу.

### Приклади

**Приклад #1 Приклад використання** get\_defined\_constants()\*\*\*\*

```php
<?php
print_r(get_defined_constants());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [E_ERROR] => 1
    [E_WARNING] => 2
    [E_PARSE] => 4
    [E_NOTICE] => 8
    [E_CORE_ERROR] => 16
    [E_CORE_WARNING] => 32
    [E_COMPILE_ERROR] => 64
    [E_COMPILE_WARNING] => 128
    [E_USER_ERROR] => 256
    [E_USER_WARNING] => 512
    [E_USER_NOTICE] => 1024
    [E_ALL] => 2047
    [TRUE] => 1
)
```

### Дивіться також

-   [defined()](function.defined.md) \- Перевіряє існування вказаної іменованої константи
-   [constant()](function.constant.md) \- Повертає значення константи
-   [get\_loaded\_extensions()](function.get-loaded-extensions.md) \- Повертає масив імен усіх скомпілованих та завантажених модулів
-   [get\_defined\_functions()](function.get-defined-functions.md) \- Повертає масив усіх певних функцій
-   [get\_defined\_vars()](function.get-defined-vars.md) \- Повертає масив усіх певних змінних
