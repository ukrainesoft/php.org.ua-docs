Інтерфейс Traversable

-   [« Вбудовані інтерфейси та класи](reserved.interfaces.html)
    
-   [Iterator »](class.iterator.html)
    
-   [PHP Manual](index.html)
    
-   [Вбудовані інтерфейси та класи](reserved.interfaces.html)
    
-   Інтерфейс Traversable
    

# Інтерфейс [Traversable](class.traversable.html)

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс, що визначає, чи є клас обхідним (traversable) з використанням [foreach](control-structures.foreach.html)

Абстрактний базовий інтерфейс, який може бути реалізований сам собою. Натомість має реалізовуватися [IteratorAggregate](class.iteratoraggregate.html) або [Iterator](class.iterator.html)

> **Зауваження**
> 
> Внутрішні (вбудовані) класи, які реалізують цей інтерфейс, можуть бути використані у конструкції [foreach](control-structures.foreach.html) і зобов'язані реалізовувати [IteratorAggregate](class.iteratoraggregate.html) або [Iterator](class.iterator.html)

> **Зауваження**
> 
> Це внутрішній інтерфейс, який може бути реалізований у скрипті PHP. Замість нього потрібно використовувати або [IteratorAggregate](class.iteratoraggregate.html), або [Iterator](class.iterator.html). При реалізації інтерфейсу, що успадковує від Traversable, переконайтеся, що у секції implements перед його ім'ям стоїть [IteratorAggregate](class.iteratoraggregate.html) або [Iterator](class.iterator.html)

## Огляд інтерфейсів

```synopsis

     
    

    
     
      interface Traversable {
   }
```

Цей інтерфейс немає методів, його єдина мета - бути базовим інтерфейсом всім обхідних класів.