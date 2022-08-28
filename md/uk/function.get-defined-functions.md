Повертає масив усіх певних функцій

-   [« function\_exists](function.function-exists.html)
    
-   [register\_shutdown\_function »](function.register-shutdown-function.html)
    
-   [PHP Manual](index.html)
    
-   [Функции управления функциями](ref.funchand.html)
    
-   Повертає масив усіх певних функцій
    

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

| Версия | Описание                                                                                     |
|--------|----------------------------------------------------------------------------------------------|
|        | Значення параметру `exclude_disabled` за умовчанням було змінено з **`false`** на **`true`** |
|        | Доданий параметр `exclude_disabled`                                                          |

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

-   [function\_exists()](function.function-exists.html) - Повертає true, якщо вказана функція визначена
-   [get\_defined\_vars()](function.get-defined-vars.html) - Повертає масив усіх певних змінних
-   [get\_defined\_constants()](function.get-defined-constants.html) - Повертає асоціативний масив з іменами всіх констант та їх значень
-   [get\_declared\_classes()](function.get-declared-classes.html) - Повертає масив із іменами оголошених класів