- [« AppendIterator::getArrayIterator](appenditerator.getarrayiterator.md)
- [AppendIterator::getIteratorIndex »](appenditerator.getiteratorindex.md)

- [PHP Manual](index.md)
- [AppendIterator](class.appenditerator.md)
- Повертає внутрішній ітератор

# AppendIterator::getInnerIterator

(PHP 5 \>= 5.1.0, PHP 7, PHP 8)

AppendIterator::getInnerIterator — Повертає внутрішній ітератор

### Опис

public **AppendIterator::getInnerIterator**():
[Iterator](class.iterator.md)

Цей спосіб повертає поточний внутрішній ітератор.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний внутрішній ітератор або **`null`**, якщо такий відсутній.

### Приклади

**Приклад #1 Приклад використання
**AppendIterator::getInnerIterator()****

` <?php$array_a = new ArrayIterator(array('a' => 'aardwolf', 'b' => 'bear', 'c' => 'capybara'));$array_b = new Regey '/^[ac]/');$iterator==new AppendIterator;$iterator->append($array_a);$iterator->append($array_b);foreach ($iterator as $current) {    $inner = ->getInnerIterator(); if ($inner instanceOf RegexIterator) {       echo 'Відфільтрований: '; } else {        echo 'Оригінальний: '; }   echo $current . PHP_EOL;}?> `

Результат виконання цього прикладу:

Оригінальний: aardwolf
Оригінальний: bear
Оригінальний: capybara
Відфільтрований: aardwolf
Відфільтрований: capybara

### Дивіться також

- [AppendIterator::getIteratorIndex()](appenditerator.getiteratorindex.md) -
Повертає індекс ітератора
