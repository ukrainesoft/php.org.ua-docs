---
navigation:
  - function.get-declared-classes.md: « get\_declared\_classes
  - function.get-declared-traits.md: get\_declared\_traits »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: get\_declared\_interfaces
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# get\_declared\_interfaces

(PHP 5, PHP 7, PHP 8)

get\_declared\_interfaces — Повертає масив усіх оголошених інтерфейсів

### Опис

```methodsynopsis
get_declared_interfaces(): array
```

Повертає оголошені інтерфейси.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає масив імен усіх оголошених інтерфейсів у скрипті.

### Приклади

**Приклад #1 Приклад використання** get\_declared\_interfaces()\*\*\*\*

```php
<?php
print_r(get_declared_interfaces());
?>
```

Висновок наведеного прикладу буде схожим на:

```
Array
(
    [0] => Traversable
    [1] => IteratorAggregate
    [2] => Iterator
    [3] => ArrayAccess
    [4] => reflector
    [5] => RecursiveIterator
    [6] => SeekableIterator
)
```

### Дивіться також

-   [interface\_exists()](function.interface-exists.md) \- Перевіряє, чи визначено інтерфейс
-   [get\_declared\_classes()](function.get-declared-classes.md) \- Повертає масив із іменами оголошених класів
-   [class\_implements()](function.class-implements.md) \- Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
