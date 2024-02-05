---
navigation:
  - ds-queue.toarray.md: '« Ds\\Queue::toArray'
  - ds-priorityqueue.allocate.md: 'Ds\\PriorityQueue::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас PriorityQueue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас PriorityQueue

(PECL ds >= 1.0.0)

## Вступ

Черга з пріоритетом дуже схожа на звичайну чергу. Значення додаються в чергу із заданим пріоритетом, і значення з вищим пріоритетом завжди будуть ближче до початку.

Реалізовано з використанням максимальної купи.

> **Зауваження** :
> 
> Порядок FIFO зберігається у значень із однаковим пріоритетом.

> **Зауваження** :
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

-   [Ds\\PriorityQueue::allocate](ds-priorityqueue.allocate.md)— Виділяє пам'ять під зазначену місткість
-   [Ds\\PriorityQueue::capacity](ds-priorityqueue.capacity.md)— Повертає поточну місткість
-   [Ds\\PriorityQueue::clear](ds-priorityqueue.clear.md) \- Видаляє всі значення
-   [Ds\\PriorityQueue::\_\_construct](ds-priorityqueue.construct.md) \- Створює новий екземпляр
-   [Ds\\PriorityQueue::copy](ds-priorityqueue.copy.md)— Повертає поверхневу копію черги
-   [Ds\\PriorityQueue::count](ds-priorityqueue.count.md)— Повертає кількість елементів у черзі
-   [Ds\\PriorityQueue::isEmpty](ds-priorityqueue.isempty.md)— Перевіряє, чи колекція порожня.
-   [Ds\\PriorityQueue::jsonSerialize](ds-priorityqueue.jsonserialize.md)— Повертає колекцію в JSON-виставу
-   [Ds\\PriorityQueue::peek](ds-priorityqueue.peek.md)— Повертає значення з початку черги
-   [Ds\\PriorityQueue::pop](ds-priorityqueue.pop.md)— Видаляє та повертає значення з найвищим пріоритетом
-   [Ds\\PriorityQueue::push](ds-priorityqueue.push.md)— Додає значення у чергу
-   [Ds\\PriorityQueue::toArray](ds-priorityqueue.toarray.md) \- Перетворює чергу на масив (array)
