---
navigation:
  - ref.scoutapm.md: « Функции Scoutapm
  - function.scoutapm-list-instrumented-functions.md: scoutapmlistinstrumentedfunctions »
  - index.md: PHP Manual
  - ref.scoutapm.md: Функции Scoutapm
title: scoutapmgetcalls
---
# scoutapmgetcalls

(PECL scoutapm >= 1.0.0)

scoutapmgetcalls — Повертає список дзвінків, що відбулися

### Опис

```methodsynopsis
scoutapm_get_calls(): array
```

Повертає список усіх дзвінків використаних функцій з моменту останнього дзвінка **scoutapmgetcalls()**. Список очищується щоразу під час виклику функції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**scoutapmgetcalls()** повертає масив, що містить список усіх записаних дзвінків використаних функцій.

### Приклади

**Приклад #1 Отримання використаних функцій**

```php
<?php

file_get_contents('a.txt');
file_get_contents('b.txt');

print_r(scoutapm_get_calls());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
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
```
