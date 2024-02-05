---
navigation:
  - parentiterator.rewind.md: '« ParentIterator::rewind'
  - recursivearrayiterator.getchildren.md: 'RecursiveArrayIterator::getChildren »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RecursiveArrayIterator
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас RecursiveArrayIterator

(PHP 5 >= 5.1.0, PHP 7, PHP 8)

## Вступ

Цей ітератор дозволяє скинути та змінити значення та ключі під час проходу масивами та об'єктами так само, як і [ArrayIterator](class.arrayiterator.md). Також можна перебирати поточні записи ітератора.

## Огляд класів

```classsynopsis

    
     class RecursiveArrayIterator
    

    
     extends
      ArrayIterator
    

    
     implements
      RecursiveIterator {

    /* Наследуемые константы */
    
     public
     const
     int
      ArrayIterator::STD_PROP_LIST;
public
     const
     int
      ArrayIterator::ARRAY_AS_PROPS;


    /* Константы */
    public
     const
     int
      CHILD_ARRAYS_ONLY;


    /* Методы */
    
   public getChildren(): ?RecursiveArrayIterator
public hasChildren(): bool


    /* Наследуемые методы */
    public ArrayIterator::__construct(array|object $array = [], int $flags = 0)

    public ArrayIterator::append(mixed $value): void
public ArrayIterator::asort(int $flags = SORT_REGULAR): true
public ArrayIterator::count(): int
public ArrayIterator::current(): mixed
public ArrayIterator::getArrayCopy(): array
public ArrayIterator::getFlags(): int
public ArrayIterator::key(): string|int|null
public ArrayIterator::ksort(int $flags = SORT_REGULAR): true
public ArrayIterator::natcasesort(): true
public ArrayIterator::natsort(): true
public ArrayIterator::next(): void
public ArrayIterator::offsetExists(mixed $key): bool
public ArrayIterator::offsetGet(mixed $key): mixed
public ArrayIterator::offsetSet(mixed $key, mixed $value): void
public ArrayIterator::offsetUnset(mixed $key): void
public ArrayIterator::rewind(): void
public ArrayIterator::seek(int $offset): void
public ArrayIterator::serialize(): string
public ArrayIterator::setFlags(int $flags): void
public ArrayIterator::uasort(callable $callback): true
public ArrayIterator::uksort(callable $callback): true
public ArrayIterator::unserialize(string $data): void
public ArrayIterator::valid(): bool

   }
```

## Обумовлені константи

## Прапори RecursiveArrayIterator

**`RecursiveArrayIterator::CHILD_ARRAYS_ONLY`**

Застосуємо лише до масивів (не об'єктів) як дітей для ітерації.

## Зміст

-   [RecursiveArrayIterator::getChildren](recursivearrayiterator.getchildren.md)— Повертає ітератор для поточного елемента, якщо елемент є масивом (array) або об'єктом (object)
-   [RecursiveArrayIterator::hasChildren](recursivearrayiterator.haschildren.md)— Визначає, чи є поточний елемент масивом чи об'єктом
