Клас Stack

-   [« Ds\\Set::xor](ds-set.xor.html)
    
-   [Ds\\Stack::allocate »](ds-stack.allocate.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Клас Stack
    

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
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.html) |

## Зміст

-   [Ds\\Stack::allocate](ds-stack.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [Ds\\Stack::capacity](ds-stack.capacity.html) — Повертає поточну місткість
-   [Ds\\Stack::clear](ds-stack.clear.html) — Видаляє всі значення з колекції
-   [Ds\\Stack::\_\_construct](ds-stack.construct.html) - Створює новий екземпляр класу
-   [Ds\\Stack::copy](ds-stack.copy.html) — Повертає поверхневу копію колекції
-   [Ds\\Stack::count](ds-stack.count.html) — Повертає кількість елементів колекції
-   [Ds\\Stack::isEmpty](ds-stack.isempty.html) — Перевіряє, чи колекція порожня.
-   [Ds\\Stack::jsonSerialize](ds-stack.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [Ds\\Stack::peek](ds-stack.peek.html) — Повертає значення з вершини стека
-   [Ds\\Stack::pop](ds-stack.pop.html) — Видаляє та повертає значення з вершини стека
-   [Ds\\Stack::push](ds-stack.push.html) — Додає значення у стек
-   [Ds\\Stack::toArray](ds-stack.toarray.html) — Перетворює колекцію на масив (array)