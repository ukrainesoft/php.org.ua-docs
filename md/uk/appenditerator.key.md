Повертає поточний ключ

-   [« AppendIterator::getIteratorIndex](appenditerator.getiteratorindex.html)
    
-   [AppendIterator::next »](appenditerator.next.html)
    
-   [PHP Manual](index.html)
    
-   [AppendIterator](class.appenditerator.html)
    
-   Повертає поточний ключ
    

# AppendIterator::key

(PHP 5> = 5.1.0, PHP 7, PHP 8)

AppendIterator::key — Повертає поточний ключ

### Опис

```methodsynopsis
public AppendIterator::key(): scalar
```

Повертає ключ.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Поточний ключ, якщо він є дійсним, або **`null`** в іншому випадку.

### Приклади

**Приклад #1 Приклад використання **AppendIterator::key()****

```php
<?php
$array_a = new ArrayIterator(array('a' => 'aardwolf', 'b' => 'bear', 'c' => 'capybara'));
$array_b = new ArrayIterator(array('apple', 'orange', 'lemon'));

$iterator = new AppendIterator;
$iterator->append($array_a);
$iterator->append($array_b);

// Ручная итерация
$iterator->rewind();
while ($iterator->valid()) {
    echo $iterator->key() . ' ' . $iterator->current() . PHP_EOL;
    $iterator->next();
}

echo PHP_EOL;

// С конструкцией foreach
foreach ($iterator as $key => $current) {
    echo $key . ' ' . $current . PHP_EOL;
}
?>
```

Результат виконання цього прикладу:

```
a aardwolf
b bear
c capybara
0 apple
1 orange
2 lemon

a aardwolf
b bear
c capybara
0 apple
1 orange
2 lemon
```

### Дивіться також

-   [Iterator::key()](iterator.key.html) - Повертає ключ поточного елемента
-   [AppendIterator::current()](appenditerator.current.html) - Повертає поточне значення
-   [AppendIterator::valid()](appenditerator.valid.html) - Перевіряє термін дії поточного елемента
-   [AppendIterator::next()](appenditerator.next.html) - Переходить до наступного елементу
-   [AppendIterator::rewind()](appenditerator.rewind.html) - перемотує ітератор