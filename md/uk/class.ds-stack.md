---
navigation:
  - ds-set.xor.md: '« Ds\\Set::xor'
  - ds-stack.allocate.md: 'Ds\\Stack::allocate »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Клас Stack
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Stack

(PECL ds >= 1.0.0)

## Вступ

Стек - це колекція типу "Останній увійшов, перший вийшов" (Last In, First Out або LIFO), яка дозволяє працювати тільки з найвищим (останнім) значенням. Ітерація походить від кінця на початок з видаленням взятого елемента.

Внутри себя использует класс[Ds\\Vector](class.ds-vector.md)

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

| Версия | Опис |
| --- | --- |
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.md) |

## Зміст

-   [Ds\\Stack::allocate](ds-stack.allocate.md)— Виділяє пам'ять під зазначену місткість
-   [Ds\\Stack::capacity](ds-stack.capacity.md)— Повертає поточну місткість
-   [Ds\\Stack::clear](ds-stack.clear.md)— Видаляє всі значення з колекції
-   [Ds\\Stack::\_\_construct](ds-stack.construct.md) \- Створює новий екземпляр класу
-   [Ds\\Stack::copy](ds-stack.copy.md)— Повертає поверхневу копію колекції
-   [Ds\\Stack::count](ds-stack.count.md)— Повертає кількість елементів колекції
-   [Ds\\Stack::isEmpty](ds-stack.isempty.md)— Перевіряє, чи колекція порожня.
-   [Ds\\Stack::jsonSerialize](ds-stack.jsonserialize.md)— Повертає колекцію в JSON-представництві
-   [Ds\\Stack::peek](ds-stack.peek.md)— Повертає значення з вершини стека
-   [Ds\\Stack::pop](ds-stack.pop.md)— Видаляє та повертає значення з вершини стека
-   [Ds\\Stack::push](ds-stack.push.md)— Додає значення у стек
-   [Ds\\Stack::toArray](ds-stack.toarray.md)— Перетворює колекцію на масив (array)
