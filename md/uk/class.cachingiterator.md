---
navigation:
  - arrayiterator.valid.md: '« ArrayIterator::valid'
  - cachingiterator.construct.md: 'CachingIterator::\_\_construct »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас CachingIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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
      ArrayAccess,

     Countable,

     Stringable {

    /* Константы */
    
     public
     const
     int
      CALL_TOSTRING;

    public
     const
     int
      CATCH_GET_CHILD;

    public
     const
     int
      TOSTRING_USE_KEY;

    public
     const
     int
      TOSTRING_USE_CURRENT;

    public
     const
     int
      TOSTRING_USE_INNER;

    public
     const
     int
      FULL_CACHE;


    /* Методы */
    
   public __construct(Iterator $iterator, int $flags = CachingIterator::CALL_TOSTRING)

    public count(): int
public current(): mixed
public getCache(): array
public getFlags(): void
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

Використати [ключ](cachingiterator.key.md)при преобразовании в строку.

**`CachingIterator::TOSTRING_USE_CURRENT`**

Використати [поточний елемент](cachingiterator.current.md)при преобразовании в строку.

**`CachingIterator::TOSTRING_USE_INNER`**

Використати [внутрішній ітератор](iteratoriterator.getinneriterator.md)при преобразовании в строку.

**`CachingIterator::FULL_CACHE`**

Кешування всієї прочитаної інформації.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Класс**CachingIterator** тепер реалізує інтерфейс [Stringable](class.stringable.md) |

## Зміст

-   [CachingIterator::\_\_construct](cachingiterator.construct.md)— Створює новий об'єкт CachingIterator для ітератора
-   [CachingIterator::count](cachingiterator.count.md)— Повертає кількість елементів в ітераторі
-   [CachingIterator::current](cachingiterator.current.md)— Повертає поточний елемент
-   [CachingIterator::getCache](cachingiterator.getcache.md)— Отримання вмісту кешу
-   [CachingIterator::getFlags](cachingiterator.getflags.md)— Отримує прапори, що використовуються.
-   [CachingIterator::hasNext](cachingiterator.hasnext.md)— Перевіряє, чи внутрішній ітератор має допустимий наступний елемент
-   [CachingIterator::key](cachingiterator.key.md)— Повертає ключ до поточного елемента
-   [CachingIterator::next](cachingiterator.next.md)— Переміщує ітератор до наступного елемента
-   [CachingIterator::offsetExists](cachingiterator.offsetexists.md)— Призначення offsetExists
-   [CachingIterator::offsetGet](cachingiterator.offsetget.md) \- Призначення offsetGet
-   [CachingIterator::offsetSet](cachingiterator.offsetset.md) \- Призначення offsetSet
-   [CachingIterator::offsetUnset](cachingiterator.offsetunset.md) \- Призначення offsetUnset
-   [CachingIterator::rewind](cachingiterator.rewind.md)— Повертає ітератор на початок
-   [CachingIterator::setFlags](cachingiterator.setflags.md)— Встановлює прапори для об'єкта CachingIterator
-   [CachingIterator::\_\_function toString() { \[native code\] }](cachingiterator.tostring.md)— Повертає строкове представлення поточного елемента
-   [CachingIterator::valid](cachingiterator.valid.md)— Перевіряє, чи поточний елемент є допустимим
