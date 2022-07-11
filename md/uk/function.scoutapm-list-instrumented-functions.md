- [« scoutapm_get_calls](function.scoutapm-get-calls.md)
- [SNMP »](book.snmp.md)

- [PHP Manual](index.md)
- [Функції Scoutapm](ref.scoutapm.md)
- Список функцій, які scoutapm буде використовувати

# scoutapm_list_instrumented_functions

(PECL scoutapm \>= 1.0.2)

scoutapm_list_instrumented_functions — Список функцій, які scoutapm
буде використовувати

### Опис

**scoutapm_list_instrumented_functions**(): array

Повертає список функцій, які модуль використовуватиме

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

**scoutapm_list_instrumented_functions()** повертає масив, що містить
Список всіх функцій, які модуль scoutapm може використовувати в
поточної установки.

### Приклади

**Приклад #1 Отримання списку функцій, які scoutapm може
використовувати**

` <?phpprint_r(scoutapm_list_instrumented_functions());?> `

Результатом виконання цього прикладу буде щось подібне:

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
