Клас CachingIterator

-   [« ArrayIterator::valid](arrayiterator.valid.html)
    
-   [CachingIterator::\_\_construct »](cachingiterator.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Итераторы](spl.iterators.html)
    
-   Клас CachingIterator
    

# Клас CachingIterator

(PHP 5, PHP 7, PHP 8)

## Вступ

Цей об'єкт підтримує кешування ітерації над іншим ітератором.

## Огляд класів

```classsynopsis

     
    

    
     
      class CachingIterator
     

     
      extends
       IteratorIterator
     

     implements 
       ArrayAccess,  Countable,  Stringable {

    /* Константы */
    
     const
     int
      CALL_TOSTRING = 1;

    const
     int
      CATCH_GET_CHILD = 16;

    const
     int
      TOSTRING_USE_KEY = 2;

    const
     int
      TOSTRING_USE_CURRENT = 4;

    const
     int
      TOSTRING_USE_INNER = 8;

    const
     int
      FULL_CACHE = 256;


    /* Методы */
    
   public __construct(Iterator $iterator, int $flags = CachingIterator::CALL_TOSTRING)

    public count(): int
public current(): mixed
public getCache(): array
public getFlags(): void
public getInnerIterator(): Iterator
public hasNext(): bool
public key(): scalar
public next(): void
public offsetExists(string $key): bool
public offsetGet(string $key): mixed
public offsetSet(string $key, mixed $value): void
public offsetUnset(string $key): void
public rewind(): void
public setFlags(int $flags): void
public __toString(): string
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

## Обумовлені константи

**`CachingIterator::CALL_TOSTRING`**

Перетворює кожен елемент на рядок.

**`CachingIterator::CATCH_GET_CHILD`**

Не викидати виключення під час доступу до дочірніх елементів.

**`CachingIterator::TOSTRING_USE_KEY`**

Використати [ключ](cachingiterator.key.html) при перетворенні на рядок.

**`CachingIterator::TOSTRING_USE_CURRENT`**

Використати [текущий элемент](cachingiterator.current.html) при перетворенні на рядок.

**`CachingIterator::TOSTRING_USE_INNER`**

Використати [внутренний итератор](cachingiterator.getinneriterator.html) при перетворенні на рядок.

**`CachingIterator::FULL_CACHE`**

Кешування всієї прочитаної інформації.

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **CachingIterator** тепер реалізує інтерфейс [Stringable](class.stringable.html) |

## Зміст

-   [CachingIterator::\_\_construct](cachingiterator.construct.html) — Створює новий об'єкт CachingIterator для ітератора
-   [CachingIterator::count](cachingiterator.count.html) — Повертає кількість елементів в ітераторі
-   [CachingIterator::current](cachingiterator.current.html) — Повертає поточний елемент
-   [CachingIterator::getCache](cachingiterator.getcache.html) — Отримання вмісту кешу
-   [CachingIterator::getFlags](cachingiterator.getflags.html) — Отримує прапори, що використовуються.
-   [CachingIterator::getInnerIterator](cachingiterator.getinneriterator.html) - Повертає внутрішній ітератор
-   [CachingIterator::hasNext](cachingiterator.hasnext.html) — Перевіряє, чи внутрішній ітератор має допустимий наступний елемент
-   [CachingIterator::key](cachingiterator.key.html) — Повертає ключ до поточного елемента
-   [CachingIterator::next](cachingiterator.next.html) — Переміщує ітератор до наступного елемента
-   [CachingIterator::offsetExists](cachingiterator.offsetexists.html) — Призначення offsetExists
-   [CachingIterator::offsetGet](cachingiterator.offsetget.html) - Призначення offsetGet
-   [CachingIterator::offsetSet](cachingiterator.offsetset.html) - Призначення offsetSet
-   [CachingIterator::offsetUnset](cachingiterator.offsetunset.html) - Призначення offsetUnset
-   [CachingIterator::rewind](cachingiterator.rewind.html) — Повертає ітератор на початок
-   [CachingIterator::setFlags](cachingiterator.setflags.html) — Встановлює прапори для об'єкта CachingIterator
-   [CachingIterator::\_\_toString](cachingiterator.tostring.html) — Повертає строкове представлення поточного елемента
-   [CachingIterator::valid](cachingiterator.valid.html) — Перевіряє, чи поточний елемент є допустимим