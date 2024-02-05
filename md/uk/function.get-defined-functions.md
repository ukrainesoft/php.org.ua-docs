---
navigation:
  - function.function-exists.md: « function\_exists
  - function.register-shutdown-function.md: register\_shutdown\_function »
  - index.md: PHP Manual
  - ref.funchand.md: Функції керування функціями
title: get\_defined\_functions
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_defined\_functions

(PHP 4 >= 4.0.4, PHP 5, PHP 7, PHP 8)

get\_defined\_functions — Повертає масив усіх функцій

### Опис

```methodsynopsis
get_defined_functions(bool $exclude_disabled = true): array
```

Отримує масив усіх функцій.

### Список параметрів

`exclude_disabled`

Чи слід виключати з результату вимкнені функції.

### Значення, що повертаються

Ця функція повертає багатовимірний масив, що містить список всіх певних функцій, як вбудованих (внутрішніх), так і користувацьких. Внутрішні функції будуть перелічені в елементі масиву $arr\["internal"\], а певні користувачем - в елементі $arr\["user"\](смотрите Приклад ниже).

### список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Значение параметра`exclude_disabled` за умовчанням було змінено з **`false`**на**`true`** |
| 7.0.15, 7.1.1 | Добавлен параметр`exclude_disabled` |

### Приклади

**Приклад #1 Приклад використання** get\_defined\_functions()\*\*\*\*

```php
<?php
function myrow($id, $data)
{
    return "<tr><th>$id</th><td>$data</td></tr>\n";
}

$arr = get_defined_functions();

print_r($arr);
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [internal] => Array
        (
            [0] => zend_version
            [1] => func_num_args
            [2] => func_get_arg
            [3] => func_get_args
            [4] => strlen
            [5] => strcmp
            [6] => strncmp
            ...
            [750] => bcscale
            [751] => bccomp
        )

    [user] => Array
        (
            [0] => myrow
        )

)
```

### Дивіться також

-   [function\_exists()](function.function-exists.md) \- Повертає true, якщо вказана функція визначена
-   [get\_defined\_vars()](function.get-defined-vars.md) \- Повертає масив усіх певних змінних
-   [get\_defined\_constants()](function.get-defined-constants.md) \- Повертає асоціативний масив з іменами всіх констант та їх значень
-   [get\_declared\_classes()](function.get-declared-classes.md) \- Повертає масив із іменами оголошених класів
