---
navigation:
  - ds-queue.toarray.md: '« DsQueue::toArray'
  - ds-priorityqueue.allocate.md: 'ДсPriorityQueue::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас PriorityQueue
---
# Клас PriorityQueue

(No version information available, might only be in Git)

## Вступ

Черга з пріоритетом дуже схожа на звичайну чергу. Значення додаються в чергу із заданим пріоритетом, і значення з вищим пріоритетом завжди будуть ближче до початку.

Реалізовано з використанням максимальної купи.

> **Зауваження**
> 
> Порядок FIFO зберігається у значень із однаковим пріоритетом.

> **Зауваження**
> 
> Ітерація через чергу відбувається із видаленням взятого елемента. Еквівалентно використанню оператора pop, доки черга не стане порожньою.

## Огляд класів

```classsynopsis


    
    
     
      class Ds\PriorityQueue
     

     implements 
       Ds\Collection {
    
    /* Константы */
    
     const
     int
      MIN_CAPACITY = 8;


    /* Методы */
    
   public allocate(int $capacity): void
public capacity(): int
public clear(): void
public copy(): Ds\PriorityQueue
public isEmpty(): bool
public peek(): mixed
public pop(): mixed
public push(mixed $value, int $priority): void
public toArray(): array

   }
```

## Обумовлені константи

**`Ds\PriorityQueue::MIN_CAPACITY`**

## Зміст

-   [ДсPriorityQueue::allocate](ds-priorityqueue.allocate.md) — Виділяє пам'ять під зазначену місткість
-   [ДсPriorityQueue::capacity](ds-priorityqueue.capacity.md) — Повертає поточну місткість
-   [ДсPriorityQueue::clear](ds-priorityqueue.clear.md) - Видаляє всі значення
-   [ДсPriorityQueue::construct](ds-priorityqueue.construct.md) - Створює новий екземпляр
-   [ДсPriorityQueue::copy](ds-priorityqueue.copy.md) — Повертає поверхневу копію черги
-   [ДсPriorityQueue::count](ds-priorityqueue.count.md) — Повертає кількість елементів у черзі
-   [ДсPriorityQueue::isEmpty](ds-priorityqueue.isempty.md) — Перевіряє, чи колекція порожня.
-   [ДсPriorityQueue::jsonSerialize](ds-priorityqueue.jsonserialize.md) — Повертає колекцію в JSON-виставу
-   [ДсPriorityQueue::peek](ds-priorityqueue.peek.md) — Повертає значення із початку черги
-   [ДсPriorityQueue::pop](ds-priorityqueue.pop.md) — Видаляє та повертає значення з найвищим пріоритетом
-   [ДсPriorityQueue::push](ds-priorityqueue.push.md) — Додає значення у чергу
-   [ДсPriorityQueue::toArray](ds-priorityqueue.toarray.md) - Перетворює чергу на масив (array)
