- [« ArrayObject::getFlags](arrayobject.getflags.md)
- [ArrayObject::getIteratorClass »](arrayobject.getiteratorclass.md)

- [PHP Manual](index.md)
- [ArrayObject](class.arrayobject.md)
- Створити новий ітератор із екземпляра ArrayObject

# ArrayObject::getIterator

(PHP 5, PHP 7, PHP 8)

ArrayObject::getIterator — Створити новий ітератор із екземпляра
ArrayObject

### Опис

public **ArrayObject::getIterator**(): [Iterator](class.iterator.md)

Створити новий ітератор із екземпляра
[ArrayObject](class.arrayobject.md).

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ітератор із [ArrayObject](class.arrayobject.md).

### Приклади

**Приклад #1 Приклад використання **ArrayObject::getIterator()****

`<?ph=$              | $arrayobject->getIterator();while($iterator->valid()) {    echo $iterator->key() . ' => ' . $iterator->current() . "
";   $iterator->next();}?> `

Результат виконання цього прикладу:

1 => один
2 => two
3 => three
