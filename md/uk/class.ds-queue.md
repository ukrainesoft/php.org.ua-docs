---
navigation:
  - ds-stack.toarray.md: '« Ds\\Stack::toArray'
  - ds-queue.allocate.md: 'Ds\\Queue::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Queue
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Queue

(PECL ds >= 1.0.0)

## Вступ

Черга - це колекція типу "Перший увійшов, перший вийшов" (First In, First Out або FIFO), яка дозволяє працювати тільки з першим значенням. Ітерація походить від початку до кінця з видаленням взятого елемента.

## Огляд класів

```classsynopsis


    
    
     
      class Ds\Queue
     

     implements 
       Ds\Collection,  ArrayAccess {
    
    /* Константы */
    
     const
     int
      MIN_CAPACITY = 8;


    /* Методы */
    
   public allocate(int $capacity): void
public capacity(): int
public clear(): void
public copy(): Ds\Queue
public isEmpty(): bool
public peek(): mixed
public pop(): mixed
public push(mixed ...$values): void
public toArray(): array

   }
```

## Обумовлені константи

**`Ds\Queue::MIN_CAPACITY`**

## список змін

| Версия | Опис |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [Ds\\Queue::allocate](ds-queue.allocate.md)— Виділяє пам'ять під зазначену місткість
-   [Ds\\Queue::capacity](ds-queue.capacity.md)— Повертає поточну місткість
-   [Ds\\Queue::clear](ds-queue.clear.md) \- Видаляє всі значення
-   [Ds\\Queue::\_\_construct](ds-queue.construct.md) \- Створює новий екземпляр
-   [Ds\\Queue::copy](ds-queue.copy.md)— Повертає поверхневу копію черги
-   [Ds\\Queue::count](ds-queue.count.md)— Повертає кількість елементів черги
-   [Ds\\Queue::isEmpty](ds-queue.isempty.md)— Перевіряє, чи колекція порожня.
-   [Ds\\Queue::jsonSerialize](ds-queue.jsonserialize.md)— Повертає колекцію в JSON-представництві
-   [Ds\\Queue::peek](ds-queue.peek.md)— Повертає значення з початку черги
-   [Ds\\Queue::pop](ds-queue.pop.md)— Видаляє та повертає значення з початку черги
-   [Ds\\Queue::push](ds-queue.push.md)— Додає значення у чергу
-   [Ds\\Queue::toArray](ds-queue.toarray.md)— Перетворює колекцію на масив (array)
