Список функцій, які scoutapm буде використовувати

-   [« scoutapmgetcalls](function.scoutapm-get-calls.html)
    
-   [SNMP »](book.snmp.md)
    
-   [PHP Manual](index.md)
    
-   [Функции Scoutapm](ref.scoutapm.md)
    
-   Список функцій, які scoutapm буде використовувати
    

# scoutapmlistinstrumentedфункцій

(PECL scoutapm >= 1.0.2)

scoutapmlistinstrumentedfunctions — Список функцій, які scoutapm використовуватиме

### Опис

```methodsynopsis
scoutapm_list_instrumented_functions(): array
```

Повертає список функцій, які модуль використовуватиме

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**scoutapmlistinstrumentedfunctions()** повертає масив, що містить список всіх функцій, які модуль scoutapm може використовувати у поточній установці.

### Приклади

**Приклад #1 Отримання списку функцій, які може використовувати scoutapm**

```php
<?php
print_r(scoutapm_list_instrumented_functions());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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