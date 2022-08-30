Клас NoRewindIterator

-   [« MultipleIterator::valid](multipleiterator.valid.md)
    
-   [NoRewindIterator::construct »](norewinditerator.construct.md)
    
-   [PHP Manual](index.md)
    
-   [Ітератори](spl.iterators.md)
    
-   Клас NoRewindIterator
    

# Клас NoRewindIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

Ітератор ігнорує операції перемотування. Це дозволяє обробляти ітератор у кількох часткових циклах начому.

## Огляд класів

```classsynopsis

     
    

    
     
      class NoRewindIterator
     

     
      extends
       IteratorIterator
     
     {

    /* Методы */
    
   public __construct(Iterator $iterator)

    public current(): mixed
public getInnerIterator(): iterator
public key(): mixed
public next(): void
public rewind(): void
public valid(): bool


    /* Наследуемые методы */
    public IteratorIterator::current(): mixed
public IteratorIterator::getInnerIterator(): ?Iterator
public IteratorIterator::key(): mixed
public IteratorIterator::next(): void
public IteratorIterator::rewind(): void
public IteratorIterator::valid(): bool

   }
```

## Зміст

-   [NoRewindIterator::construct](norewinditerator.construct.md) — Створює новий об'єкт NoRewindIterator
-   [NoRewindIterator::current](norewinditerator.current.md) — Отримує поточне значення
-   [NoRewindIterator::getInnerIterator](norewinditerator.getinneriterator.md) — Отримує внутрішній ітератор
-   [NoRewindIterator::key](norewinditerator.key.md) — Отримує поточний ключ
-   [NoRewindIterator::next](norewinditerator.next.md) — Переміщує ітератор до наступного елемента
-   [NoRewindIterator::rewind](norewinditerator.rewind.md) — Запобігає поверненню внутрішнього ітератора на початок
-   [NoRewindIterator::valid](norewinditerator.valid.md) - Перевіряє ітератор