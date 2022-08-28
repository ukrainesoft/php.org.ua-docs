Інтерфейс SeekableIterator

-   [« RecursiveIterator::hasChildren](recursiveiterator.haschildren.html)
    
-   [SeekableIterator::seek »](seekableiterator.seek.html)
    
-   [PHP Manual](index.html)
    
-   [Интерфейсы](spl.interfaces.html)
    
-   Інтерфейс SeekableIterator
    

# Інтерфейс SeekableIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Ітератор Seekable.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface SeekableIterator
      extends
       Iterator
     
     {

    /* Методы */
    
   public seek(int $offset): void


    /* Наследуемые методы */
    public Iterator::current(): mixed
public Iterator::key(): mixed
public Iterator::next(): void
public Iterator::rewind(): void
public Iterator::valid(): bool

   }
```

**Приклад #1 Просте використання**

Цей приклад демонструє створення користувальницького ітератора **SeekableIterator**, який шукає позицію та обробляє недійсну позицію.

```php
<?php
class MySeekableIterator implements SeekableIterator {

    private $position;

    private $array = array(
        "первый элемент",
        "второй элемент",
        "третий элемент",
        "четвёртый элемент"
    );

    /* Метод, требуемый для интерфейса SeekableIterator */

    public function seek($position) {
      if (!isset($this->array[$position])) {
          throw new OutOfBoundsException("недействительная позиция ($position)");
      }

      $this->position = $position;
    }

    /*  Методы, требуемые для интерфейса Iterator */

    public function rewind() {
        $this->position = 0;
    }

    public function current() {
        return $this->array[$this->position];
    }

    public function key() {
        return $this->position;
    }

    public function next() {
        ++$this->position;
    }

    public function valid() {
        return isset($this->array[$this->position]);
    }
}

try {

    $it = new MySeekableIterator;
    echo $it->current(), "\n";

    $it->seek(2);
    echo $it->current(), "\n";

    $it->seek(1);
    echo $it->current(), "\n";

    $it->seek(10);

} catch (OutOfBoundsException $e) {
    echo $e->getMessage();
}
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
первый элемент
третий элемент
второй элемент
недействительная позиция (10)
```

## Зміст

-   [SeekableIterator::seek](seekableiterator.seek.html) — Переміщається до позиції