- [« Ds\Pair::\_\_construct](ds-pair.construct.md)
- [Ds\Pair::isEmpty »](ds-pair.isempty.md)

- [PHP Manual](index.md)
- [Пара](class.ds-pair.md)
- Повертає поверхневу копію пари

# Ds\Pair::copy

(No version information available, might only be in Git)

Ds\Pair::copy — Повертає поверхневу копію пари

### Опис

public **Ds\Pair::copy**(): [Ds\Pair](class.ds-pair.md)

Повертає поверхневу копію пари.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

.

### Приклади

**Приклад #1 Приклад використання **Ds\Pair::copy()****

` <?php$a = new \Ds\Pair("a", 1);$b = $a->copy();$a->key = "x";print_r($a);print_r($ b);?> `

Результатом виконання цього прикладу буде щось подібне:

Ds\Pair Object
(
[key] => x
[value] => 1
)
Ds\Pair Object
(
[key] => a
[value] => 1
)
