---
navigation:
  - function.get-declared-classes.md: « getdeclaredclasses
  - function.get-declared-traits.md: getdeclaredtraits »
  - index.md: PHP Manual
  - ref.classobj.md: Функції роботи з класами та об'єктами
title: getdeclaredinterfaces
---
# getdeclaredinterfaces

(PHP 5, PHP 7, PHP 8)

getdeclaredinterfaces — Повертає масив усіх оголошених інтерфейсів

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

**Приклад #1 Приклад використання **getdeclaredinterfaces()****

```php
<?php
print_r(get_declared_interfaces());
?>
```

Результатом виконання цього прикладу буде щось подібне:

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

-   [interfaceexists()](function.interface-exists.md) - Перевіряє, чи визначено інтерфейс
-   [getdeclaredclasses()](function.get-declared-classes.md) - Повертає масив із іменами оголошених класів
-   [classimplements()](function.class-implements.md) - Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі
