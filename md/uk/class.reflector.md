---
navigation:
  - reflectionattribute.newinstance.html: '« ReflectionAttribute::newInstance'
  - reflector.export.html: 'Reflector::export »'
  - index.html: PHP Manual
  - book.reflection.html: Reflection
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
|  | Клас **Reflector** тепер реалізує інтерфейс [Stringable](class.stringable.html) |

## Зміст

-   [Reflector::export](reflector.export.html) - Експорт
-   [Reflector::toString](reflector.tostring.html) — Подання у вигляді рядка
