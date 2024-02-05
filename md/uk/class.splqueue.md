---
navigation:
  - class.splstack.md: « SplStack
  - splqueue.dequeue.md: 'SplQueue::dequeue »'
  - index.md: PHP Manual
  - spl.datastructures.md: Структури даних
title: Клас SplQueue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SplQueue

(PHP 5 >= 5.3.0, PHP 7, PHP 8)

## Вступ

Клас SplQueue надає основні функціональні можливості черги, реалізованої з використанням двозв'язкового списку, встановивши режим ітератора **`SplDoublyLinkedList::IT_MODE_FIFO`**

## Огляд класів

```classsynopsis

    
     class SplQueue
    

    
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


    /* Методы */
    
   public dequeue(): mixed
public enqueue(mixed $value): void


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

**Пример #1 Пример использования**SplQueue\*\*\*\*

```php
<?php
$q = new SplQueue();
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
1
2
3
```

**Приклад #2 Ефективне розв'язання задач за допомогою **SplQueue****

```php
<?php
$q = new SplQueue();
$q->setIteratorMode(SplQueue::IT_MODE_DELETE);
// ... добавление некоторых задач в очередь ...
// обработка
foreach ($q as $task) {
    // ... обработка $task ...
    // добавление новых задач в очередь
    $q[] = $newTask;
    // ...
}
?>
```

## Зміст

-   [SplQueue::dequeue](splqueue.dequeue.md)— Видаляє елемент із черги
-   [SplQueue::enqueue](splqueue.enqueue.md)— Додає елемент у чергу
