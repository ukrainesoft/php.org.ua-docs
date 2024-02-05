---
navigation:
  - recursivearrayiterator.haschildren.md: '« RecursiveArrayIterator::hasChildren'
  - recursivecachingiterator.construct.md: 'RecursiveCachingIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RecursiveCachingIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас RecursiveCachingIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

...

## Огляд класів

```classsynopsis

    
     class RecursiveCachingIterator
    

    
     extends
      CachingIterator
    

    
     implements
      RecursiveIterator {

    /* Наследуемые константы */
    
     public
     const
     int
      CachingIterator::CALL_TOSTRING;
public
     const
     int
      CachingIterator::CATCH_GET_CHILD;
public
     const
     int
      CachingIterator::TOSTRING_USE_KEY;
public
     const
     int
      CachingIterator::TOSTRING_USE_CURRENT;
public
     const
     int
      CachingIterator::TOSTRING_USE_INNER;
public
     const
     int
      CachingIterator::FULL_CACHE;


    /* Методы */
    
   public __construct(Iterator $iterator, int $flags = RecursiveCachingIterator::CALL_TOSTRING)

    public getChildren(): ?RecursiveCachingIterator
public hasChildren(): bool


    /* Наследуемые методы */
    public CachingIterator::count(): int
public CachingIterator::current(): mixed
public CachingIterator::getCache(): array
public CachingIterator::getFlags(): void
public CachingIterator::hasNext(): bool
public CachingIterator::key(): scalar
public CachingIterator::next(): void
public CachingIterator::offsetExists(string $key): bool
public CachingIterator::offsetGet(string $key): mixed
public CachingIterator::offsetSet(string $key, mixed $value): void
public CachingIterator::offsetUnset(string $key): void
public CachingIterator::rewind(): void
public CachingIterator::setFlags(int $flags): void
public CachingIterator::__toString(): string
public CachingIterator::valid(): bool

    public IteratorIterator::current(): mixed
public IteratorIterator::getInnerIterator(): ?Iterator
public IteratorIterator::key(): mixed
public IteratorIterator::next(): void
public IteratorIterator::rewind(): void
public IteratorIterator::valid(): bool

   }
```

## Зміст

-   [RecursiveCachingIterator::\_\_construct](recursivecachingiterator.construct.md) \- Конструктор
-   [RecursiveCachingIterator::getChildren](recursivecachingiterator.getchildren.md)— Повертає дочірні елементи внутрішнього ітератора у вигляді об'єкта RecursiveCachingIterator
-   [RecursiveCachingIterator::hasChildren](recursivecachingiterator.haschildren.md)— Перевіряє, чи має поточний елемент внутрішнього ітератора дочірні елементи
