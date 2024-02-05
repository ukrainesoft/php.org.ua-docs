---
navigation:
  - reflectionattribute.newinstance.md: '« ReflectionAttribute::newInstance'
  - reflector.export.md: 'Reflector::export »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Інтерфейс Reflector
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Інтерфейс Reflector

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс **Reflector** реалізують всі експортовані Reflection-класи.

## Огляд інтерфейсів

```classsynopsis

    
     interface Reflector

    extends
      Stringable {

    /* Наследуемые методы */
    
   public Stringable::__toString(): string

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[Reflector::export()](reflector.export.md)був видалений. |
| 8.0.0 | Класс**Reflector** тепер успадковує [Stringable](class.stringable.md). . Він успадковує [Stringable::\_\_toString()](stringable.tostring.md), замінюючи **Reflector::\_\_toString()** |

## Дивіться також

-   [Reflector::export()](reflector.export.md)

## Зміст

-   [Reflector::export](reflector.export.md) \- Експорт
