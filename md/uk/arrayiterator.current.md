- [«ArrayIterator::count](arrayiterator.count.md)
- [ArrayIterator::getArrayCopy »](arrayiterator.getarraycopy.md)

- [PHP Manual](index.md)
- [ArrayIterator](class.arrayiterator.md)
- Повертає поточний елемент у масиві

# ArrayIterator::current

(PHP 5, PHP 7, PHP 8)

ArrayIterator::current — Повертає поточний елемент у масиві

### Опис

public **ArrayIterator::current**():
[mixed](language.types.declarations.md#language.types.declarations.mixed)

Повертає поточний елемент масиву (array).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний елемент масиву (array).

### Приклади

**Приклад #1 Приклад використання **ArrayIterator::current()****

`<?ph=$array = array('1' => 'one',   y| iterator= $arrayobject->getIterator();   $iterator->valid();   $iterator->next()) {    echo $iterator->key() . ' => ' . $iterator->current() . "
";}?> `

Результат виконання цього прикладу:

1 => один
2 => two
3 => three
