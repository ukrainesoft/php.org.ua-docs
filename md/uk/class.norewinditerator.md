---
navigation:
  - multipleiterator.valid.md: '« MultipleIterator::valid'
  - norewinditerator.construct.md: 'NoRewindIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас NoRewindIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас NoRewindIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

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

-   [NoRewindIterator::\_\_construct](norewinditerator.construct.md)— Створює новий об'єкт NoRewindIterator
-   [NoRewindIterator::current](norewinditerator.current.md)— Отримує поточне значення
-   [NoRewindIterator::key](norewinditerator.key.md)— Отримує поточний ключ
-   [NoRewindIterator::next](norewinditerator.next.md)— Переміщує ітератор до наступного елемента
-   [NoRewindIterator::rewind](norewinditerator.rewind.md)— Запобігає поверненню внутрішнього ітератора на початок
-   [NoRewindIterator::valid](norewinditerator.valid.md) \- Перевіряє ітератор
