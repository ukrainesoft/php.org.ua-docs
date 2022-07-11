- [« Функції Xhprof](ref.xhprof.md)
- [xhprof_enable »](function.xhprof-enable.md)

- [PHP Manual](index.md)
- [Функції Xhprof](ref.xhprof.md)
- Зупиняє профіль xhprof

#xhprof_disable

(PECL xhprof \>= 0.9.0)

xhprof_disable — Зупиняє профіль xhprof

### Опис

**xhprof_disable**(): array

Зупиняє профіль та повертає зібрані дані.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Масив із результатами профілювання.

### Приклади

**Приклад #1 Приклад використання **xhprof_disable()****

` <?phpxhprof_enable();$foo = strlen("foo bar");$xhprof_data = xhprof_disable();print_r($xhprof_data);?> `

Результатом виконання цього прикладу буде щось подібне:

Array
(
[main()==>strlen] => Array
(
[ct] => 1
[wt] => 279
)

[main()==>xhprof_disable] => Array
(
[ct] => 1
[wt] => 9
)

[main()] => Array
(
[ct] => 1
[wt] => 610
)

)
