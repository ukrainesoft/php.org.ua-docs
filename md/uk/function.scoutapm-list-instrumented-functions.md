---
navigation:
  - function.scoutapm-get-calls.md: « scoutapm\_get\_calls
  - book.snmp.md: SNMP »
  - index.md: PHP Manual
  - ref.scoutapm.md: Функції Scoutapm
title: scoutapm\_list\_instrumented\_functions
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# scoutapm\_list\_instrumented\_functions

(PECL scoutapm >= 1.0.2)

scoutapm\_list\_instrumented\_functions — Список функцій, які scoutapm використовуватиме

### Опис

```methodsynopsis
scoutapm_list_instrumented_functions(): array
```

Повертає список функцій, які модуль використовуватиме

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**scoutapm\_list\_instrumented\_functions()** повертає масив, що містить список усіх функцій, які модуль scoutapm може використовувати у поточній установці.

### Приклади

**Приклад #1 Отримання списку функцій, які може використовувати scoutapm**

```php
<?php
print_r(scoutapm_list_instrumented_functions());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => file_get_contents
    [1] => file_put_contents
    [2] => fopen
    [3] => fread
    [4] => fwrite
    [5] => pdo->exec
    [6] => pdo->query
    [7] => pdo->prepare
    [8] => pdostatement->execute
)
```
