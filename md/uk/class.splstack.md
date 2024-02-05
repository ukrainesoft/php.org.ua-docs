---
navigation:
  - spldoublylinkedlist.valid.md: '« SplDoublyLinkedList::valid'
  - class.splqueue.md: SplQueue »
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplStack
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SplStack

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplStack надає основні функціональні можливості стека, реалізовані з використанням двозв'язкового списку, встановивши режим ітератора **`SplDoublyLinkedList::IT_MODE_LIFO`**

## Огляд класів

```classsynopsis

    
     class SplStack
    

    
     extends
      SplDoublyLinkedList
     {

    /* Наследуемые константы */
    
     public
     const
     int
      SplDoublyLinkedList::IT_MODE_LIFO;
public
     const
     int
      SplDoublyLinkedList::IT_MODE_FIFO;
public
     const
     int
      SplDoublyLinkedList::IT_MODE_DELETE;
public
     const
     int
      SplDoublyLinkedList::IT_MODE_KEEP;


    /* Наследуемые методы */
    
   public SplDoublyLinkedList::add(int $index, mixed $value): void
public SplDoublyLinkedList::bottom(): mixed
public SplDoublyLinkedList::count(): int
public SplDoublyLinkedList::current(): mixed
public SplDoublyLinkedList::getIteratorMode(): int
public SplDoublyLinkedList::isEmpty(): bool
public SplDoublyLinkedList::key(): int
public SplDoublyLinkedList::next(): void
public SplDoublyLinkedList::offsetExists(int $index): bool
public SplDoublyLinkedList::offsetGet(int $index): mixed
public SplDoublyLinkedList::offsetSet(?int $index, mixed $value): void
public SplDoublyLinkedList::offsetUnset(int $index): void
public SplDoublyLinkedList::pop(): mixed
public SplDoublyLinkedList::prev(): void
public SplDoublyLinkedList::push(mixed $value): void
public SplDoublyLinkedList::rewind(): void
public SplDoublyLinkedList::serialize(): string
public SplDoublyLinkedList::setIteratorMode(int $mode): int
public SplDoublyLinkedList::shift(): mixed
public SplDoublyLinkedList::top(): mixed
public SplDoublyLinkedList::unserialize(string $data): void
public SplDoublyLinkedList::unshift(mixed $value): void
public SplDoublyLinkedList::valid(): bool

   }
```

## Приклади

**Приклад #1 Приклад використання** SplStack\*\*\*\*

```php
<?php
$q = new SplStack();
$q[] = 1;
$q[] = 2;
$q[] = 3;
foreach ($q as $elem)  {
 echo $elem."\n";
}
?>
```

Результат виконання наведеного прикладу:

```
3
2
1
```
