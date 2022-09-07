---
navigation:
  - parentiterator.rewind.md: '« ParentIterator::rewind'
  - recursivearrayiterator.getchildren.md: 'RecursiveArrayIterator::getChildren »'
  - index.md: PHP Manual
  - spl.iterators.md: Ітератори
title: Клас RecursiveArrayIterator
---
# Клас RecursiveArrayIterator

(PHP 5> = 5.1.0, PHP 7, PHP 8)

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
    
     const
     int
      STD_PROP_LIST = 1;
const
     int
      ARRAY_AS_PROPS = 2;


    /* Константы */
    const
     int
      CHILD_ARRAYS_ONLY = 4;


    /* Методы */
    
   public getChildren(): ?RecursiveArrayIterator
public hasChildren(): bool


    /* Наследуемые методы */
    public ArrayIterator::append(mixed $value): void
public ArrayIterator::asort(int $flags = SORT_REGULAR): bool
public ArrayIterator::count(): int
public ArrayIterator::current(): mixed
public ArrayIterator::getArrayCopy(): array
public ArrayIterator::getFlags(): int
public ArrayIterator::key(): string|int|null
public ArrayIterator::ksort(int $flags = SORT_REGULAR): bool
public ArrayIterator::natcasesort(): bool
public ArrayIterator::natsort(): bool
public ArrayIterator::next(): void
public ArrayIterator::offsetExists(mixed $key): bool
public ArrayIterator::offsetGet(mixed $key): mixed
public ArrayIterator::offsetSet(mixed $key, mixed $value): void
public ArrayIterator::offsetUnset(mixed $key): void
public ArrayIterator::rewind(): void
public ArrayIterator::seek(int $offset): void
public ArrayIterator::serialize(): string
public ArrayIterator::setFlags(int $flags): void
public ArrayIterator::uasort(callable $callback): bool
public ArrayIterator::uksort(callable $callback): bool
public ArrayIterator::unserialize(string $data): void
public ArrayIterator::valid(): bool

   }
```

## Обумовлені константи

## Прапори RecursiveArrayIterator

**`RecursiveArrayIterator::CHILD_ARRAYS_ONLY`**

Застосуємо лише до масивів (не об'єктів) як дітей для ітерації.

## Зміст

-   [RecursiveArrayIterator::getChildren](recursivearrayiterator.getchildren.md) — Повертає ітератор для поточного елемента, якщо елемент є масивом (array) або об'єктом (object)
-   [RecursiveArrayIterator::hasChildren](recursivearrayiterator.haschildren.md) — Визначає, чи є поточний елемент масивом чи об'єктом
