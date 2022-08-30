Клас ReflectionType

-   [« ReflectionProperty::toString](reflectionproperty.tostring.html)
    
-   [ReflectionType::allowsNull »](reflectiontype.allowsnull.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionType
    

# Клас ReflectionType

(PHP 7, PHP 8)

## Вступ

Клас **ReflectionType** повідомляє інформацію про тип параметра/повертається значення функції або тип властивості класу. Модуль Reflection оголошує такі підтипи:

-   [ReflectionNamedType](class.reflectionnamedtype.html) (починаючи з PHP 7.1.0)
-   [ReflectionUnionType](class.reflectionuniontype.html) (починаючи з PHP 8.0.0)
-   [ReflectionIntersectionType](class.reflectionintersectiontype.html) (починаючи з PHP 8.1.0)

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

| Версия | Описание                                                                                                                                                              |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|        | **ReflectionType** став абстрактним, а метод **ReflectionType::isBuiltin()** був переміщений у [ReflectionNamedType::isBuiltin()](reflectionnamedtype.isbuiltin.html) |

## Зміст

-   [ReflectionType::allowsNull](reflectiontype.allowsnull.html) — Перевіряє, чи допустимо NULL
-   [ReflectionType::toString](reflectiontype.tostring.html) — Перетворення на рядок