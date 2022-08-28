Клас RecursiveCachingIterator

-   [« RecursiveArrayIterator::hasChildren](recursivearrayiterator.haschildren.html)
    
-   [RecursiveCachingIterator::\_\_construct »](recursivecachingiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
-   Клас RecursiveCachingIterator
    

# Клас RecursiveCachingIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class RecursiveCachingIterator
     

     
      extends
       CachingIterator
     

     implements 
       RecursiveIterator {

    /* Наследуемые константы */
    
     const
     int
      CachingIterator::CALL_TOSTRING = 1;
const
     int
      CachingIterator::CATCH_GET_CHILD = 16;
const
     int
      CachingIterator::TOSTRING_USE_KEY = 2;
const
     int
      CachingIterator::TOSTRING_USE_CURRENT = 4;
const
     int
      CachingIterator::TOSTRING_USE_INNER = 8;
const
     int
      CachingIterator::FULL_CACHE = 256;


    /* Методы */
    
   public __construct(Iterator $iterator, int $flags = RecursiveCachingIterator::CALL_TOSTRING)

    public getChildren(): ?RecursiveCachingIterator
public hasChildren(): bool


    /* Наследуемые методы */
    public CachingIterator::count(): int
public CachingIterator::current(): mixed
public CachingIterator::getCache(): array
public CachingIterator::getFlags(): void
public CachingIterator::getInnerIterator(): Iterator
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

-   [RecursiveCachingIterator::\_\_construct](recursivecachingiterator.construct.html) - Конструктор
-   [RecursiveCachingIterator::getChildren](recursivecachingiterator.getchildren.html) — Повертає дочірні елементи внутрішнього ітератора у вигляді об'єкта RecursiveCachingIterator
-   [RecursiveCachingIterator::hasChildren](recursivecachingiterator.haschildren.html) — Перевіряє, чи має поточний елемент внутрішнього ітератора дочірні елементи