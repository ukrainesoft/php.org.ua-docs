---
navigation:
  - ds.examples.md: « Приклади
  - ds-collection.clear.md: 'Ds\\Collection::clear »'
  - index.md: PHP Manual
  - book.ds.md: Структури даних
title: Інтерфейс Collection
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Collection

(PECL ds >= 1.0.0)

## Вступ

**Collection** - це базовий інтерфейс, який покриває функціональність загальну всім структур даних у цій бібліотеці. Він гарантує, що всі структури обхідні, лічильний і можуть бути перетворені на JSON за допомогою функції [json\_encode()](function.json-encode.md)

## Огляд інтерфейсів

```classsynopsis

    interface Ds\Collection

    extends
      Countable,
     IteratorAggregate,
     JsonSerializable {

    /* Методы */
    
   public clear(): void
public copy(): Ds\Collection
public isEmpty(): bool
public toArray(): array


    /* Наследуемые методы */
    public Countable::count(): int

    public IteratorAggregate::getIterator(): Traversable

    public JsonSerializable::jsonSerialize(): mixed


   }
```

## список змін

| Версия | Опис |
| --- | --- |
| PECL ds 1.4.0 | Класс**Collection** тепер реалізує інтерфейс [IteratorAggregate](class.iteratoraggregate.md) замість [Traversable](class.traversable.md). . (Ця зміна з'явилася у поліфілі у версії 1.4.1). |

## Зміст

-   [Ds\\Collection::clear](ds-collection.clear.md) \- Видаляє всі значення
-   [Ds\\Collection::copy](ds-collection.copy.md)— Повертає копію колекції
-   [Ds\\Collection::isEmpty](ds-collection.isempty.md)— Перевіряє, чи колекція порожня.
-   [Ds\\Collection::toArray](ds-collection.toarray.md)— Перетворює колекцію на масив (array)
