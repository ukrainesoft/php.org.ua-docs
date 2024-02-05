---
navigation:
  - class.recursivefilteriterator.md: « RecursiveFilterIterator
  - recursivefilteriterator.getchildren.md: 'RecursiveFilterIterator::getChildren »'
  - index.md: PHP Manual
  - class.recursivefilteriterator.md: RecursiveFilterIterator
title: 'RecursiveFilterIterator::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# RecursiveFilterIterator::\_\_construct

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

RecursiveFilterIterator::\_\_construct — Створює об'єкт RecursiveFilterIterator на основі об'єкта-ітератора RecursiveIterator

### Опис

public **RecursiveFilterIterator::\_\_construct** [RecursiveIterator](class.recursiveiterator.md) `$iterator`) .

Створює ітератор [RecursiveFilterIterator](class.recursivefilteriterator.md)на основе[RecursiveIterator](class.recursiveiterator.md)

### Список параметрів

`iterator`

Об'єкт-ітератор [RecursiveIterator](class.recursiveiterator.md)елементи якого потрібно відфільтрувати.

### Приклади

**Приклад #1 Приклад використання** RecursiveFilterIterator()\*\*\*\*

```php
<?php
class TestsOnlyFilter extends RecursiveFilterIterator {
    public function accept() {
        // текущий элемент пройдёт фильтр, если имеет дочерние элементы или
        // его значение начинается со строки "test"
        return $this->hasChildren() || (strpos($this->current(), "test") !== FALSE);
    }
}

$array    = array("test1", array("taste2", "test3", "test4"), "test5");
$iterator = new RecursiveArrayIterator($array);
$filter   = new TestsOnlyFilter($iterator);

foreach(new RecursiveIteratorIterator($filter) as $key => $value)
{
    echo $value . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
test1
test3
test4
test5
```

**Приклад #2 Ще приклад з **RecursiveFilterIterator()****

```php
<?php
class StartsWithFilter extends RecursiveFilterIterator {

    protected $word;

    public function __construct(RecursiveIterator $rit, $word) {
        $this->word = $word;
        parent::__construct($rit);
    }

    public function accept() {
        return $this->hasChildren() OR strpos($this->current(), $this->word) === 0;
    }

    public function getChildren() {
        return new self($this->getInnerIterator()->getChildren(), $this->word);
    }
}

$array    = array("test1", array("taste2", "test3", "test4"), "test5");
$iterator = new RecursiveArrayIterator($array);
$filter   = new StartsWithFilter($iterator, "test");

foreach(new RecursiveIteratorIterator($filter) as $key => $value)
{
    echo $value . "\n";
}
?>
```

Висновок наведеного прикладу буде схожим на:

```
test1
test3
test4
test5
```

### Дивіться також

-   [RecursiveFilterIterator::getChildren()](recursivefilteriterator.getchildren.md) \- Повертає дочірні елементи внутрішнього ітератора у вигляді об'єкта RecursiveFilterIterator
-   [RecursiveFilterIterator::hasChildren()](recursivefilteriterator.haschildren.md) \- Перевіряє, чи має поточний елемент внутрішнього ітератора дочірні елементи
-   [FilterIterator::accept()](filteriterator.accept.md) \- Перевіряє, чи є поточний елемент ітератора допустимим
