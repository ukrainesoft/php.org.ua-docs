---
navigation:
  - spldoublylinkedlist.valid.html: '« SplDoublyLinkedList::valid'
  - splstack.construct.html: 'SplStack::construct »'
  - index.html: PHP Manual
  - spl.datastructures.html: Структури даних
title: Клас SplStack
---
# Клас SplStack

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplStack надає основні функціональні можливості стека, реалізовані за допомогою двозв'язкового списку.

## Огляд класів

```classsynopsis

     
    

    
     
      class SplStack
     

     
      extends
       SplDoublyLinkedList
     
     {

    /* Методы */
    
   public __construct()

    public setIteratorMode(int $mode): void


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

## Зміст

-   [SplStack::construct](splstack.construct.html) — Створює новий стек, реалізований за допомогою двозв'язкового списку
-   [SplStack::setIteratorMode](splstack.setiteratormode.html) - Встановлює режим ітератора
