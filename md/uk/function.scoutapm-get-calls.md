---
navigation:
  - ref.scoutapm.md: « Функції Scoutapm
  - function.scoutapm-list-instrumented-functions.md: scoutapm\_list\_instrumented\_functions »
  - index.md: PHP Manual
  - ref.scoutapm.md: Функції Scoutapm
title: scoutapm\_get\_calls
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# scoutapm\_get\_calls

(PECL scoutapm >= 1.0.0)

scoutapm\_get\_calls — Повертає список дзвінків, що відбулися

### Опис

```methodsynopsis
scoutapm_get_calls(): array
```

Повертає список усіх дзвінків використаних функцій з моменту останнього дзвінка **scoutapm\_get\_calls()**. Список очищується щоразу під час виклику функції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**scoutapm\_get\_calls()** повертає масив, що містить список усіх записаних дзвінків використаних функцій.

### Приклади

**Приклад #1 Отримання використаних функцій**

```php
<?php

file_get_contents('a.txt');
file_get_contents('b.txt');

print_r(scoutapm_get_calls());
?>
```

Висновок наведеного прикладу буде схожим на:

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
