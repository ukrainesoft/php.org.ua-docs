---
navigation:
  - reflectionproperty.tostring.md: '« ReflectionProperty::toString'
  - reflectiontype.allowsnull.md: 'ReflectionType::allowsNull »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionType
---
# Клас ReflectionType

(PHP 7, PHP 8)

## Вступ

Клас **ReflectionType** повідомляє інформацію про тип параметра/повертається значення функції або тип властивості класу. Модуль Reflection оголошує такі підтипи:

-   [ReflectionNamedType](class.reflectionnamedtype.md) (починаючи з PHP 7.1.0)
-   [ReflectionUnionType](class.reflectionuniontype.md) (починаючи з PHP 8.0.0)
-   [ReflectionIntersectionType](class.reflectionintersectiontype.md) (починаючи з PHP 8.1.0)

## Огляд класів

```classsynopsis

     
    

    
     
      abstract
      class ReflectionType
     

     implements 
       Stringable {

    /* Методы */
    
   public allowsNull(): bool
public __toString(): string

   }
```

## список змін

| Версия | Описание |
| --- | --- |
|  | **ReflectionType** став абстрактним, а метод **ReflectionType::isBuiltin()** був переміщений у [ReflectionNamedType::isBuiltin()](reflectionnamedtype.isbuiltin.md) |

## Зміст

-   [ReflectionType::allowsNull](reflectiontype.allowsnull.md) — Перевіряє, чи допустимо NULL
-   [ReflectionType::toString](reflectiontype.tostring.md) — Перетворення на рядок
