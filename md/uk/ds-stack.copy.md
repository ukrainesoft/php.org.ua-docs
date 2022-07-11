- [« Ds\Stack::\_\_construct](ds-stack.construct.md)
- [Ds\Stack::count »](ds-stack.count.md)

- [PHP Manual](index.md)
- [Стек](class.ds-stack.md)
- Повертає поверхневу копію колекції

# Ds\Stack::copy

(PECL ds \>= 1.0.0)

Ds\Stack::copy — Повертає поверхневу копію колекції

### Опис

public **Ds\Stack::copy**(): [Ds\Stack](class.ds-stack.md)

Повертає поверхневу копію колекції.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Колекція поверхнева копія.

### Приклади

**Приклад #1 Приклад використання **Ds\Stack::copy()****

` <?php$a = new \Ds\Stack([1, 2, 3]);$b = $a->copy();// Зміна копії не відбивається на оригіналі$b->push(4); print_r($a);print_r($b);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Stack Object
(
[0] => 3
[1] => 2
[2] => 1
)
Ds\Stack Object
(
[0] => 4
[1] => 3
[2] => 2
[3] => 1
)
