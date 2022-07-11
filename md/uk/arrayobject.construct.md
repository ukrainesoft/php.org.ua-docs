- [« ArrayObject::asort](arrayobject.asort.md)
- [ArrayObject::count »](arrayobject.count.md)

- [PHP Manual](index.md)
- [ArrayObject](class.arrayobject.md)
- Створює новий об'єкт масиву

# ArrayObject::\_\_construct

(PHP 5, PHP 7, PHP 8)

ArrayObject::\_\_construct — Створює новий об'єкт масиву

### Опис

public **ArrayObject::\_\_construct**(array\|object `$array` = [], int
`$flags` = 0, string `$iteratorClass` = ArrayIterator::class)

Створює новий об'єкт масиву.

### Список параметрів

`array`
Параметр array приймає значення типу array або Object.

`flags`
Прапори для керування поведінкою об'єкта [ArrayObject](class.arrayobject.md). Дивіться
[ArrayObject::setFlags()](arrayobject.setflags.md).

`iteratorClass`
Вказує клас, який використовуватиметься як ітератор
об'єкта [ArrayObject](class.arrayobject.md). Клас повинен реалізувати
інтерфейс [Iterator](class.iterator.md).

### Приклади

**Приклад #1 Приклад використання **ArrayObject::\_\_construct()****

`<?ph=$array = array('1' => 'one',  | arrayobject);?> `

Результат виконання цього прикладу:

object(ArrayObject)#1 (3) {
[1]=>
string(3) "one"
[2]=>
string(3) "two"
[3]=>
string(5) "three"
}

### Дивіться також

- [ArrayObject::setflags()](arrayobject.setflags.md) - Встановлює
прапори поведінки
