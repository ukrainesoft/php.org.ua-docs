Клас Queue

-   [« Ds\\Stack::toArray](ds-stack.toarray.html)
    
-   [Ds\\Queue::allocate »](ds-queue.allocate.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Клас Queue
    

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

| Версия        | Описание                                                  |
|---------------|-----------------------------------------------------------|
| PECL ds 1.3.0 | Тепер клас реалізує [ArrayAccess](class.arrayaccess.html) |

## Зміст

-   [Ds\\Queue::allocate](ds-queue.allocate.html) — Виділяє пам'ять під зазначену місткість
-   [Ds\\Queue::capacity](ds-queue.capacity.html) — Повертає поточну місткість
-   [Ds\\Queue::clear](ds-queue.clear.html) - Видаляє всі значення
-   [Ds\\Queue::\_\_construct](ds-queue.construct.html) - Створює новий екземпляр
-   [Ds\\Queue::copy](ds-queue.copy.html) — Повертає поверхневу копію черги
-   [Ds\\Queue::count](ds-queue.count.html) — Повертає кількість елементів черги
-   [Ds\\Queue::isEmpty](ds-queue.isempty.html) — Перевіряє, чи колекція порожня.
-   [Ds\\Queue::jsonSerialize](ds-queue.jsonserialize.html) — Повертає колекцію в JSON-представництві
-   [Ds\\Queue::peek](ds-queue.peek.html) — Повертає значення із початку черги
-   [Ds\\Queue::pop](ds-queue.pop.html) — Видаляє та повертає значення з початку черги
-   [Ds\\Queue::push](ds-queue.push.html) - Додає значення в чергу
-   [Ds\\Queue::toArray](ds-queue.toarray.html) — Перетворює колекцію на масив (array)