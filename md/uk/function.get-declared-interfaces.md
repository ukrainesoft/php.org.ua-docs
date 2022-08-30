Повертає масив усіх оголошених інтерфейсів

-   [« getdeclaredclasses](function.get-declared-classes.html)
    
-   [getdeclaredtraits »](function.get-declared-traits.html)
    
-   [PHP Manual](index.html)
    
-   [Функції роботи з класами та об'єктами](ref.classobj.html)
    
-   Повертає масив усіх оголошених інтерфейсів
    

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

-   [interfaceexists()](function.interface-exists.html) - Перевіряє, чи визначено інтерфейс
-   [getdeclaredclasses()](function.get-declared-classes.html) - Повертає масив із іменами оголошених класів
-   [classimplements()](function.class-implements.html) - Повертає список інтерфейсів, реалізованих у заданому класі чи інтерфейсі