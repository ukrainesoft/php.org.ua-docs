Клас NoRewindIterator

-   [« MultipleIterator::valid](multipleiterator.valid.html)
    
-   [NoRewindIterator::\_\_construct »](norewinditerator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
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

-   [NoRewindIterator::\_\_construct](norewinditerator.construct.html) — Створює новий об'єкт NoRewindIterator
-   [NoRewindIterator::current](norewinditerator.current.html) — Отримує поточне значення
-   [NoRewindIterator::getInnerIterator](norewinditerator.getinneriterator.html) — Отримує внутрішній ітератор
-   [NoRewindIterator::key](norewinditerator.key.html) — Отримує поточний ключ
-   [NoRewindIterator::next](norewinditerator.next.html) — Переміщує ітератор до наступного елемента
-   [NoRewindIterator::rewind](norewinditerator.rewind.html) — Запобігає поверненню внутрішнього ітератора на початок
-   [NoRewindIterator::valid](norewinditerator.valid.html) - Перевіряє ітератор