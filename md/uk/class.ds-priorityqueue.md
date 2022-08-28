Клас PriorityQueue

-   [« Ds\\Queue::toArray](ds-queue.toarray.html)
    
-   [Ds\\PriorityQueue::allocate »](ds-priorityqueue.allocate.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Клас PriorityQueue
    

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

-   [Ds\\PriorityQueue::allocate](ds-priorityqueue.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [Ds\\PriorityQueue::capacity](ds-priorityqueue.capacity.html) — Повертає поточну місткість
-   [Ds\\PriorityQueue::clear](ds-priorityqueue.clear.html) - Видаляє всі значення
-   [Ds\\PriorityQueue::\_\_construct](ds-priorityqueue.construct.html) - Створює новий екземпляр
-   [Ds\\PriorityQueue::copy](ds-priorityqueue.copy.html) — Повертає поверхневу копію черги
-   [Ds\\PriorityQueue::count](ds-priorityqueue.count.html) — Повертає кількість елементів у черзі
-   [Ds\\PriorityQueue::isEmpty](ds-priorityqueue.isempty.html) — Перевіряє, чи колекція порожня.
-   [Ds\\PriorityQueue::jsonSerialize](ds-priorityqueue.jsonserialize.html) — Повертає колекцію в JSON-виставу
-   [Ds\\PriorityQueue::peek](ds-priorityqueue.peek.html) — Повертає значення із початку черги
-   [Ds\\PriorityQueue::pop](ds-priorityqueue.pop.html) — Видаляє та повертає значення з найвищим пріоритетом
-   [Ds\\PriorityQueue::push](ds-priorityqueue.push.html) — Додає значення у чергу
-   [Ds\\PriorityQueue::toArray](ds-priorityqueue.toarray.html) - Перетворює чергу на масив (array)