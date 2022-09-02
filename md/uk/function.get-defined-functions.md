---
navigation:
  - function.function-exists.md: « functionexists
  - function.register-shutdown-function.md: registershutdownfunction »
  - index.md: PHP Manual
  - ref.funchand.md: Функции управления функциями
title: getdefinedфункцій
---
# getdefinedфункцій

(PHP 4> = 4.0.4, PHP 5, PHP 7, PHP 8)

getdefinedfunctions — Повертає масив усіх функцій

### Опис

```methodsynopsis
get_defined_functions(bool $exclude_disabled = true): array
```

Отримує масив усіх функцій.

### Список параметрів

`exclude_disabled`

Чи слід виключати з результату вимкнені функції.

### Значення, що повертаються

Ця функція повертає багатовимірний масив, що містить список всіх певних функцій, як вбудованих (внутрішніх), так і користувацьких. Внутрішні функції будуть перелічені в елементі масиву $arr"internal", а певні користувачем - в елементі $arr"user" (Дивіться приклад нижче).

### список змін

| Версия | Описание |
| --- | --- |
|  | Значення параметру `exclude_disabled` за умовчанням було змінено з **`false`** на **`true`** |
|  | Доданий параметр `exclude_disabled` |

### Приклади

**Приклад #1 Приклад використання **getdefinedfunctions()****

```php
<?php
function myrow($id, $data)
{
    return "<tr><th>$id</th><td>$data</td></tr>\n";
}

$arr = get_defined_functions();

print_r($arr);
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [functionexists()](function.function-exists.md) - Повертає true, якщо вказана функція визначена
-   [getdefinedvars()](function.get-defined-vars.md) - Повертає масив усіх певних змінних
-   [getdefinedconstants()](function.get-defined-constants.md) - Повертає асоціативний масив з іменами всіх констант та їх значень
-   [getdeclaredclasses()](function.get-declared-classes.md) - Повертає масив із іменами оголошених класів
