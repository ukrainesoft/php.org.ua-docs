---
navigation:
  - reserved.interfaces.md: « Вбудовані інтерфейси та класи
  - class.iterator.md: Iterator »
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: 'Інтерфейс [Traversable](class.traversable.md)'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс [Traversable](class.traversable.md)

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс, що визначає, чи клас обхідним (traversable) з використанням [foreach](control-structures.foreach.md)

Абстрактний базовий інтерфейс, який може бути реалізований сам собою. Натомість має реалізовуватися [IteratorAggregate](class.iteratoraggregate.md) або [Iterator](class.iterator.md)

## Огляд інтерфейсів

```classsynopsis

    
     interface Traversable {
   }
```

Цей інтерфейс немає методів, його єдина мета - бути базовим інтерфейсом всім обхідних класів.

## список змін

| Версия | Опис |
| --- | --- |
| 7.4.0 | Інтерфейс **Traversable** тепер може бути реалізований абстрактними класами. Класи, що розширюються, повинні реалізовувати інтерфейс [Iterator](class.iterator.md) або [IteratorAggregate](class.iteratoraggregate.md) |

## Примітки

> **Зауваження** :
> 
> Внутрішні (вбудовані) класи, що реалізують цей інтерфейс, можуть бути використані у конструкції [foreach](control-structures.foreach.md) і повинні реалізовувати інтерфейс [IteratorAggregate](class.iteratoraggregate.md) або [Iterator](class.iterator.md)

> **Зауваження** :
> 
> До версії PHP 7.4.0 цей внутрішній інтерфейс двигуна не міг бути реалізований в PHP-скриптах. Замість нього слід використовувати або інтерфейс [IteratorAggregate](class.iteratoraggregate.md), либо[Iterator](class.iterator.md)
