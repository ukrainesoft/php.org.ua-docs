---
navigation:
  - ds-stack.toarray.html: '« DsStack::toArray'
  - ds-queue.allocate.html: 'ДсQueue::allocate »'
  - index.html: PHP Manual
  - book.ds.html: Структури даних
title: Клас Queue
---
# Клас Queue

(No version information available, might only be in Git)

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

| Версия | Описание |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [ДсQueue::allocate](ds-queue.allocate.md) — Виділяє пам'ять під зазначену місткість
-   [ДсQueue::capacity](ds-queue.capacity.md) — Повертає поточну місткість
-   [ДсQueue::clear](ds-queue.clear.md) - Видаляє всі значення
-   [ДсQueue::construct](ds-queue.construct.md) - Створює новий екземпляр
-   [ДсQueue::copy](ds-queue.copy.md) — Повертає поверхневу копію черги
-   [ДсQueue::count](ds-queue.count.md) — Повертає кількість елементів черги
-   [ДсQueue::isEmpty](ds-queue.isempty.md) — Перевіряє, чи колекція порожня.
-   [ДсQueue::jsonSerialize](ds-queue.jsonserialize.md) — Повертає колекцію в JSON-представництві
-   [ДсQueue::peek](ds-queue.peek.md) — Повертає значення із початку черги
-   [ДсQueue::pop](ds-queue.pop.md) — Видаляє та повертає значення з початку черги
-   [ДсQueue::push](ds-queue.push.md) - Додає значення в чергу
-   [ДсQueue::toArray](ds-queue.toarray.md) — Перетворює колекцію на масив (array)
