---
navigation:
  - ds.examples.html: « Приклади
  - ds-collection.clear.html: 'ДсCollection::clear »'
  - index.html: PHP Manual
  - book.ds.html: Структури даних
title: Інтерфейс Collection
---
# Інтерфейс Collection

(No version information available, might only be in Git)

## Вступ

**Collection** - це базовий інтерфейс, який покриває функціональність загальну всім структур даних у цій бібліотеці. Він гарантує, що всі структури обхідні, лічильний і можуть бути перетворені на JSON за допомогою функції [jsonencode()](function.json-encode.md)

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
| PECL ds 1.4.0 | Клас **Collection** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.html) замість [Traversable](class.traversable.md). (Ця зміна з'явилася у поліфілі у версії 1.4.1). |

## Зміст

-   [ДсCollection::clear](ds-collection.clear.md) - Видаляє всі значення
-   [ДсCollection::copy](ds-collection.copy.md) — Повертає копію колекції
-   [ДсCollection::isEmpty](ds-collection.isempty.md) — Перевіряє, чи колекція порожня.
-   [ДсCollection::toArray](ds-collection.toarray.md) — Перетворює колекцію на масив (array)
