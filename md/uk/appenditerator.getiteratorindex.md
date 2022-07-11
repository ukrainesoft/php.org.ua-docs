- [« AppendIterator::getInnerIterator](appenditerator.getinneriterator.md)
- [AppendIterator::key »](appenditerator.key.md)

- [PHP Manual](index.md)
- [AppendIterator](class.appenditerator.md)
- Повертає індекс ітератора

# AppendIterator::getIteratorIndex

(PHP 5 \>= 5.2.0, PHP 7, PHP 8)

AppendIterator::getIteratorIndex — Повертає індекс ітератора

### Опис

public **AppendIterator::getIteratorIndex**(): ?int

Повертає індекс поточного внутрішнього ітератора.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає цілий індекс, що починається з нуля поточного
внутрішнього ітератора, якщо він існує, або **`null`** у протилежному
випадку.

### Приклади

**Приклад #1 Приклад використання **AppendIterator.getIteratorIndex()****

` <?php$array_a = new ArrayIterator(array('a' => 'aardwolf', 'b' => 'bear', 'c' => 'capybara'));$array_b = new Array' apple', 'orange', 'lemon'));$iterator = new AppendIterator;$iterator->append($array_a);$iterator->append($array_b);foreach ($iterator as $key =>  current ) {    echo $iterator->getIteratorIndex() . '  ' . $key . ' ' . $ current . PHP_EOL;}?> `

Результат виконання цього прикладу:

0 a aardwolf
0 b bear
0 c capybara
1 0 apple
1 1 orange
1 2 lemon

### Дивіться також

- [AppendIterator::getInnerIterator()](appenditerator.getinneriterator.md) -
Повертає внутрішній ітератор
- [AppendIterator::getArrayIterator()](appenditerator.getarrayiterator.md) -
Повертає клас ітератора масиву ArrayIterator
