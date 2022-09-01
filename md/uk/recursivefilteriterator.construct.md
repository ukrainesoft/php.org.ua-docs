---
navigation:
  - class.recursivefilteriterator.html: « RecursiveFilterIterator
  - recursivefilteriterator.getchildren.html: 'RecursiveFilterIterator::getChildren »'
  - index.html: PHP Manual
  - class.recursivefilteriterator.html: RecursiveFilterIterator
title: 'RecursiveFilterIterator::construct'
---
# RecursiveFilterIterator::construct

(PHP 5> = 5.1.0, PHP 7, PHP 8)

RecursiveFilterIterator::construct — Створює об'єкт RecursiveFilterIterator на основі об'єкта-ітератора RecursiveIterator

### Опис

public **RecursiveFilterIterator::construct**[RecursiveIterator](class.recursiveiterator.html) `$iterator`

Створює ітератор [RecursiveFilterIterator](class.recursivefilteriterator.html) на основі [RecursiveIterator](class.recursiveiterator.html)

### Список параметрів

`iterator`

Об'єкт-ітератор [RecursiveIterator](class.recursiveiterator.html)елементи якого потрібно відфільтрувати.

### Приклади

**Приклад #1 Приклад використання **RecursiveFilterIterator()****

```php
<?php
class TestsOnlyFilter extends RecursiveFilterIterator {
    public function accept() {
        // текущий элемент пройдёт фильтр, если имеет дочерние элементы или
        // его значение начинается со строки "test"
        return $this->hasChildren() || (strpos($this->current(), "test") !== FALSE);
    }
}

$array    = array("test1", array("taste2", "test3", "test4"), "test5");
$iterator = new RecursiveArrayIterator($array);
$filter   = new TestsOnlyFilter($iterator);

foreach(new RecursiveIteratorIterator($filter) as $key => $value)
{
    echo $value . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
test1
test3
test4
test5
```

**Приклад #2 Ще приклад з **RecursiveFilterIterator()****

```php
<?php
class StartsWithFilter extends RecursiveFilterIterator {

    protected $word;

    public function __construct(RecursiveIterator $rit, $word) {
        $this->word = $word;
        parent::__construct($rit);
    }

    public function accept() {
        return $this->hasChildren() OR strpos($this->current(), $this->word) === 0;
    }

    public function getChildren() {
        return new self($this->getInnerIterator()->getChildren(), $this->word);
    }
}

$array    = array("test1", array("taste2", "test3", "test4"), "test5");
$iterator = new RecursiveArrayIterator($array);
$filter   = new StartsWithFilter($iterator, "test");

foreach(new RecursiveIteratorIterator($filter) as $key => $value)
{
    echo $value . "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
test1
test3
test4
test5
```

### Дивіться також

-   [RecursiveFilterIterator::getChildren()](recursivefilteriterator.getchildren.html) - Повертає дочірні елементи внутрішнього ітератора у вигляді об'єкта RecursiveFilterIterator
-   [RecursiveFilterIterator::hasChildren()](recursivefilteriterator.haschildren.html) - Перевіряє, чи має поточний елемент внутрішнього ітератора дочірні елементи
-   [FilterIterator::accept()](filteriterator.accept.html) - Перевіряє, чи є поточний елемент ітератора допустимим
