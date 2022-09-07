---
navigation:
  - reflectionattribute.newinstance.md: '« ReflectionAttribute::newInstance'
  - reflector.export.md: 'Reflector::export »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Інтерфейс Reflector
---
# Інтерфейс Reflector

(PHP 5, PHP 7, PHP 8)

## Вступ

Інтерфейс **Reflector** реалізують всі експортовані Reflection-класи.

## Огляд інтерфейсів

```classsynopsis

     
    

    
     
      interface Reflector
      extends
       Stringable
     
     {


    /* Методы */
    
   public static export(): string
public __toString(): string


    /* Наследуемые методы */
    public Stringable::__toString(): string

   }
```

## список змін

| Версия | Описание |
| --- | --- |
|  | Клас **Reflector** тепер реалізує інтерфейс [Stringable](class.stringable.md) |

## Зміст

-   [Reflector::export](reflector.export.md) - Експорт
-   [Reflector::toString](reflector.tostring.md) — Подання у вигляді рядка
