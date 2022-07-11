- [«get_current_user](function.get-current-user.md)
- [get_extension_funcs »](function.get-extension-funcs.md)

- [PHP Manual](index.md)
- [Опції PHP/інформаційні функції](ref.info.md)
- Повертає асоціативний масив з іменами всіх констант та їх
значень

#get_defined_constants

(PHP 4 \>= 4.1.0, PHP 5, PHP 7, PHP 8)

get_defined_constants - Повертає асоціативний масив з іменами всіх
констант та їх значень

### Опис

**get_defined_constants**(bool `$categorize` = **`false`**): array

Повертає асоціативний масив з іменами та значеннями всіх певних
нині констант. Масив буде включати константи,
визначені модулями, а також створені функцією
[define()](function.define.md).

### Список параметрів

`categorize`
Використання цього аргументу дає можливість отримати багатовимірний
масив, в якому в першому вимірі будуть утримуватися категорії
констант, а в другому відповідні імена та значення.

` <?phpdefine("MY_CONSTANT", 1);print_r(get_defined_constants(true));?> `

Результатом виконання цього прикладу буде щось подібне:

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

### Значення, що повертаються

Повертає масив виду "ім'я константи" =\> "значення константи", з
можливістю згрупувати його на ім'я модуля, що зареєстрував
константи.

### Приклади

**Приклад #1 Приклад використання **get_defined_constants()****

` <?phpprint_r(get_defined_constants());?> `

Результатом виконання цього прикладу буде щось подібне:

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

### Дивіться також

- [defined()](function.defined.md) - Перевіряє існування
зазначеної іменованої константи
- [get_loaded_extensions()](function.get-loaded-extensions.md) -
Повертає масив імен усіх скомпілованих та завантажених модулів
- [get_defined_functions()](function.get-defined-functions.md) -
Повертає масив усіх певних функцій
- [get_defined_vars()](function.get-defined-vars.md) - Повертає
масив усіх певних змінних
