- [«function_exists](function.function-exists.md)
- [register_shutdown_function »](function.register-shutdown-function.md)

- [PHP Manual](index.md)
- [Функції керування функціями](ref.funchand.md)
- Повертає масив усіх певних функцій

#get_defined_functions

(PHP 4 \>= 4.0.4, PHP 5, PHP 7, PHP 8)

get_defined_functions — Повертає масив усіх функцій

### Опис

**get_defined_functions**(bool `$exclude_disabled` = **`true`**): array

Отримує масив усіх функцій.

### Список параметрів

`exclude_disabled`
Чи слід виключати з результату вимкнені функції.

### Значення, що повертаються

Ця функція повертає багатовимірний масив, що містить список усіх
певних функцій як вбудованих (внутрішніх), так і
користувальницьких. Внутрішні функції будуть перелічені в елементі
масиву `$arr["internal"]`, а певні користувачем - в елементі
`$arr["user"]` (див. приклад нижче).

### Список змін

| Версія        | Опис                                                                                       |
| ------------- | ------------------------------------------------------------------------------------------ |
| 8.0.0         | Значення параметра exclude_disabled за замовчуванням було змінено з **false** на **true**. |
| 7.0.15, 7.1.1 | Доданий параметр exclude_disabled.                                                         |

### Приклади

**Приклад #1 Приклад використання **get_defined_functions()****

` <?phpfunction myrow($id, $data){    return "<tr><th>$id</th><td>$data</td></tr>
";}$arr = get_defined_functions();print_r($arr);?> `

Результатом виконання цього прикладу буде щось подібне:

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

### Дивіться також

- [function_exists()](function.function-exists.md) - Повертає
true, якщо зазначена функція визначена
- [get_defined_vars()](function.get-defined-vars.md) - Повертає
масив усіх певних змінних
- [get_defined_constants()](function.get-defined-constants.md) -
Повертає асоціативний масив з іменами всіх констант та їх
значень
- [get_declared_classes()](function.get-declared-classes.md) -
Повертає масив із іменами оголошених класів
