- [«NoRewindIterator](class.norewinditerator.md)
- [NoRewindIterator::current »](norewinditerator.current.md)

- [PHP Manual](index.md)
- [NoRewindIterator](class.norewinditerator.md)
- Створює новий об'єкт NoRewindIterator

# NoRewindIterator::\_\_construct

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

NoRewindIterator::\_\_construct — Створює новий об'єкт NoRewindIterator

### Опис

public
**NoRewindIterator::\_\_construct**([Iterator](class.iterator.md)
`$iterator`)

Створює новий об'єкт NoRewindIterator.

### Список параметрів

`iterator`
Ітератор, що використовується.

### Приклади

**Приклад #1 Приклад використання **NoRewindIterator::\_\_construct()****

Другий цикл нічого не виведе, оскільки ітератор використовується лише
один раз і не може бути повернутий на початок.

` <?php$fruit = array('яблуко', 'банан', 'журавлина');$arr = new ArrayObject($fruit);$it  = new NoRewindIterator($arr->getIterator());echo А:
";foreach( $it as $item ) {    echo $item . "
";}echo "Фрукт Б:
";foreach( $it as $item ) {    echo $item . "
";}?> `

Результатом виконання цього прикладу буде щось подібне:

Фрукт А:
яблуко
банан
журавлина
Фрукт Б:

### Дивіться також

- [NoRewindIterator::valid()](norewinditerator.valid.md) - Перевіряє
ітератор
