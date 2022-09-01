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
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.html) |

## Зміст

-   [ДсQueue::allocate](ds-queue.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [ДсQueue::capacity](ds-queue.capacity.html) — Повертає поточну місткість
-   [ДсQueue::clear](ds-queue.clear.html) - Видаляє всі значення
-   [ДсQueue::construct](ds-queue.construct.html) - Створює новий екземпляр
-   [ДсQueue::copy](ds-queue.copy.html) — Повертає поверхневу копію черги
-   [ДсQueue::count](ds-queue.count.html) — Повертає кількість елементів черги
-   [ДсQueue::isEmpty](ds-queue.isempty.html) — Перевіряє, чи колекція порожня.
-   [ДсQueue::jsonSerialize](ds-queue.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [ДсQueue::peek](ds-queue.peek.html) — Повертає значення із початку черги
-   [ДсQueue::pop](ds-queue.pop.html) — Видаляє та повертає значення з початку черги
-   [ДсQueue::push](ds-queue.push.html) - Додає значення в чергу
-   [ДсQueue::toArray](ds-queue.toarray.html) — Перетворює колекцію на масив (array)
