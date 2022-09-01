---
navigation:
  - ds-set.xor.html: '« DsSet::xor'
  - ds-stack.allocate.html: 'ДсStack::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Stack
---
# Клас Stack

(No version information available, might only be in Git)

## Вступ

Стек - це колекція типу "Останній увійшов, перший вийшов" (Last In, First Out або LIFO), яка дозволяє працювати тільки з найвищим (останнім) значенням. Ітерація походить від кінця на початок з видаленням взятого елемента.

Усередині себе використовує клас **ДсVector**

## Огляд класів

```classsynopsis


    
    
     
      class Ds\Stack
     

     implements 
       Ds\Collection,  ArrayAccess {
    

    /* Методы */
    
   public allocate(int $capacity): void
public capacity(): int
public clear(): void
public copy(): Ds\Stack
public isEmpty(): bool
public peek(): mixed
public pop(): mixed
public push(mixed ...$values): void
public toArray(): array

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [ДсStack::allocate](ds-stack.allocate.md) — Виділяє пам'ять під зазначену місткість
-   [ДсStack::capacity](ds-stack.capacity.md) — Повертає поточну місткість
-   [ДсStack::clear](ds-stack.clear.md) — Видаляє всі значення з колекції
-   [ДсStack::construct](ds-stack.construct.md) - Створює новий екземпляр класу
-   [ДсStack::copy](ds-stack.copy.md) — Повертає поверхневу копію колекції
-   [ДсStack::count](ds-stack.count.md) — Повертає кількість елементів колекції
-   [ДсStack::isEmpty](ds-stack.isempty.md) — Перевіряє, чи колекція порожня.
-   [ДсStack::jsonSerialize](ds-stack.jsonserialize.md) — Повертає колекцію в JSON-представництві
-   [ДсStack::peek](ds-stack.peek.md) — Повертає значення з вершини стека
-   [ДсStack::pop](ds-stack.pop.md) — Видаляє та повертає значення з вершини стека
-   [ДсStack::push](ds-stack.push.md) — Додає значення у стек
-   [ДсStack::toArray](ds-stack.toarray.md) — Перетворює колекцію на масив (array)
