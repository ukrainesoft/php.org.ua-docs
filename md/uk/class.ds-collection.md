Інтерфейс Collection

-   [« Примеры](ds.examples.html)
    
-   [Ds\\Collection::clear »](ds-collection.clear.html)
    
-   [PHP Manual](index.html)
    
-   [Структуры данных](book.ds.html)
    
-   Інтерфейс Collection
    

# Інтерфейс Collection

(No version information available, might only be in Git)

## Вступ

**Collection** - це базовий інтерфейс, який покриває функціональність загальну всім структур даних у цій бібліотеці. Він гарантує, що всі структури обхідні, лічильний і можуть бути перетворені на JSON за допомогою функції [json\_encode()](function.json-encode.html)

## Огляд інтерфейсів

```classsynopsis


    
    

     class Ds\Collection

     implements  Countable,  IteratorAggregate,  JsonSerializable {
    

    /* Методы */
    
   abstract public clear(): void
abstract public copy(): Ds\Collection
abstract public isEmpty(): bool
abstract public toArray(): array

   }
```

## список змін

| Версия | Описание |
| --- | --- |
| PECL ds 1.4.0 | Клас **Collection** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html) замість [Traversable](class.traversable.html). (Ця зміна з'явилася у поліфілі у версії 1.4.1). |

## Зміст

-   [Ds\\Collection::clear](ds-collection.clear.html) - Видаляє всі значення
-   [Ds\\Collection::copy](ds-collection.copy.html) — Повертає копію колекції
-   [Ds\\Collection::isEmpty](ds-collection.isempty.html) — Перевіряє, чи колекція порожня.
-   [Ds\\Collection::toArray](ds-collection.toarray.html) — Перетворює колекцію на масив (array)