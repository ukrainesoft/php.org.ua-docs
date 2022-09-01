---
navigation:
  - class.traversable.md: « Traversable
  - iterator.current.md: 'Iterator::current »'
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: Інтерфейс Iterator
---
# Інтерфейс Iterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс для зовнішніх ітераторів чи об'єктів, які можуть повторювати себе зсередини.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     interface Iterator
      extends
       Traversable
     
     {

    /* Методы */
    
   public current(): mixed
public key(): mixed
public next(): void
public rewind(): void
public valid(): bool

   }
```

## Обумовлені ітератори

PHP вже надає деякі ітератори для багатьох повсякденних завдань. Дивіться список [ітераторів SPL](spl.iterators.md) для детальнішої інформації.

## Приклади

**Приклад #1 Основи використання**

Цей приклад демонструє, у якому порядку викликаються методи, коли використовується з ітератором оператор. [foreach](control-structures.foreach.md)

```php
<?php
class myIterator implements Iterator {
    private $position = 0;
    private $array = array(
        "firstelement",
        "secondelement",
        "lastelement",
    );

    public function __construct() {
        $this->position = 0;
    }

    public function rewind(): void {
        var_dump(__METHOD__);
        $this->position = 0;
    }

    #[ReturnTypeWillChange]
    public function current() {
        var_dump(__METHOD__);
        return $this->array[$this->position];
    }

    #[ReturnTypeWillChange]
    public function key() {
        var_dump(__METHOD__);
        return $this->position;
    }

    public function next(): void {
        var_dump(__METHOD__);
        ++$this->position;
    }

    public function valid(): bool {
        var_dump(__METHOD__);
        return isset($this->array[$this->position]);
    }
}

$it = new myIterator;

foreach($it as $key => $value) {
    var_dump($key, $value);
    echo "\n";
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
string(18) "myIterator::rewind"
string(17) "myIterator::valid"
string(19) "myIterator::current"
string(15) "myIterator::key"
int(0)
string(12) "firstelement"

string(16) "myIterator::next"
string(17) "myIterator::valid"
string(19) "myIterator::current"
string(15) "myIterator::key"
int(1)
string(13) "secondelement"

string(16) "myIterator::next"
string(17) "myIterator::valid"
string(19) "myIterator::current"
string(15) "myIterator::key"
int(2)
string(11) "lastelement"

string(16) "myIterator::next"
string(17) "myIterator::valid"
```

## Дивіться також

Дивіться також розділ [Ітератори об'єктів](language.oop5.iterations.md)

## Зміст

-   [Iterator::current](iterator.current.md) — Повернення поточного елемента
-   [Iterator::key](iterator.key.md) — Повертає ключ поточного елемента
-   [Iterator::next](iterator.next.md) — Переходить до наступного елементу
-   [Iterator::rewind](iterator.rewind.md) - Повертає ітератор на перший елемент
-   [Iterator::valid](iterator.valid.md) - Перевіряє коректність поточної позиції
