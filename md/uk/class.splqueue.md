Клас SplQueue

-   [« SplStack::setIteratorMode](splstack.setiteratormode.html)
    
-   [SplQueue::\_\_construct »](splqueue.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](spl.datastructures.html)
    
-   Клас SplQueue
    

# Клас SplQueue

(PHP 5> = 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplQueue надає основні функціональні можливості черги, реалізовані за допомогою двозв'язкового списку.

## Огляд класів

```classsynopsis

     
    

    
     
      class SplQueue
     

     
      extends
       SplDoublyLinkedList
     
     {

    /* Методы */
    
   public SplStack::__construct()

    public dequeue(): mixed
public enqueue(mixed $value): void
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

-   [SplQueue::\_\_construct](splqueue.construct.html) — Створює нову чергу, реалізовану за допомогою двозв'язкового списку
-   [SplQueue::dequeue](splqueue.dequeue.html) — Видаляє елемент із черги
-   [SplQueue::enqueue](splqueue.enqueue.html) — Додає елемент у чергу
-   [SplQueue::setIteratorMode](splqueue.setiteratormode.html) - Встановлює режим ітератора