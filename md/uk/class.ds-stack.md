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

-   [ДсStack::allocate](ds-stack.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [ДсStack::capacity](ds-stack.capacity.html) — Повертає поточну місткість
-   [ДсStack::clear](ds-stack.clear.html) — Видаляє всі значення з колекції
-   [ДсStack::construct](ds-stack.construct.html) - Створює новий екземпляр класу
-   [ДсStack::copy](ds-stack.copy.html) — Повертає поверхневу копію колекції
-   [ДсStack::count](ds-stack.count.html) — Повертає кількість елементів колекції
-   [ДсStack::isEmpty](ds-stack.isempty.html) — Перевіряє, чи колекція порожня.
-   [ДсStack::jsonSerialize](ds-stack.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [ДсStack::peek](ds-stack.peek.html) — Повертає значення з вершини стека
-   [ДсStack::pop](ds-stack.pop.html) — Видаляє та повертає значення з вершини стека
-   [ДсStack::push](ds-stack.push.html) — Додає значення у стек
-   [ДсStack::toArray](ds-stack.toarray.html) — Перетворює колекцію на масив (array)
