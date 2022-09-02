---
navigation:
  - reserved.interfaces.md: « Вбудовані інтерфейси та класи
  - class.iterator.md: Iterator »
  - index.md: PHP Manual
  - reserved.interfaces.md: Вбудовані інтерфейси та класи
title: 'Інтерфейс Traversable'
---
# Інтерфейс [Traversable](class.traversable.md)

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс, що визначає, чи є клас обхідним (traversable) з використанням [foreach](control-structures.foreach.md)

Абстрактний базовий інтерфейс, який може бути реалізований сам собою. Натомість має реалізовуватися [IteratorAggregate](class.iteratoraggregate.md) або [Iterator](class.iterator.md)

> **Зауваження**
> 
> Внутрішні (вбудовані) класи, які реалізують цей інтерфейс, можуть бути використані у конструкції [foreach](control-structures.foreach.md) і зобов'язані реалізовувати [IteratorAggregate](class.iteratoraggregate.md) або [Iterator](class.iterator.md)

> **Зауваження**
> 
> Це внутрішній інтерфейс, який може бути реалізований у скрипті PHP. Замість нього потрібно використовувати або [IteratorAggregate](class.iteratoraggregate.md), або [Iterator](class.iterator.md). При реалізації інтерфейсу, що успадковує від Traversable, переконайтеся, що у секції implements перед його ім'ям стоїть [IteratorAggregate](class.iteratoraggregate.md) або [Iterator](class.iterator.md)

## Огляд інтерфейсів

```synopsis

     
    

    
     
      interface Traversable {
   }
```

Цей інтерфейс немає методів, його єдина мета - бути базовим інтерфейсом всім обхідних класів.
