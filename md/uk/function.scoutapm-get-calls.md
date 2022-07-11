- [« Функції Scoutapm](ref.scoutapm.md)
- [scoutapm_list_instrumented_functions »](function.scoutapm-list-instrumented-functions.md)

- [PHP Manual](index.md)
- [Функції Scoutapm](ref.scoutapm.md)
- Повертає список викликів, що відбулися

#scoutapm_get_calls

(PECL scoutapm \>= 1.0.0)

scoutapm_get_calls — Повертає список дзвінків, що відбулися

### Опис

**scoutapm_get_calls**(): array

Повертає список усіх дзвінків використаних функцій з моменту
останнього дзвінка **scoutapm_get_calls()**. Список очищується щоразу
під час виклику функції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**scoutapm_get_calls()** повертає масив, що містить список усіх
записаних викликів використаних функцій.

### Приклади

**Приклад #1 Отримання використаних функцій**

` <?phpfile_get_contents('a.txt');file_get_contents('b.txt');print_r(scoutapm_get_calls());?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[0] => Array
(
[function] => file_get_contents
[entered] => 1576839727.7934
[exited] => 1576839727.7935
[time_taken] => 2.7894973754883E-5
[argv] => Array
(
[0] => a.txt
)

)

[1] => Array
(
[function] => file_get_contents
[entered] => 1576839727.7935
[exited] => 1576839727.7935
[time_taken] => 7.8678131103516E-6
[argv] => Array
(
[0] => b.txt
)

)

)
