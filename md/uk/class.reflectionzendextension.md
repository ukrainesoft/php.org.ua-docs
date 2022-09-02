---
navigation:
  - reflectionenumbackedcase.getbackingvalue.md: '« ReflectionEnumBackedCase::getBackingValue'
  - reflectionzendextension.clone.md: 'ReflectionZendExtension::clone »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionZendExtension
---
# Клас ReflectionZendExtension

(PHP 5> = 5.4.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionZendExtension
     

     implements 
       Reflector {

    /* Свойства */
    
     public
     string
      $name;


    /* Методы */
    
   public __construct(string $name)

    private __clone(): void
public static export(string $name, bool $return = ?): string
public getAuthor(): string
public getCopyright(): string
public getName(): string
public getURL(): string
public getVersion(): string
public __toString(): string

   }
```

## Властивості

name

Ім'я модуль. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.md) під час спроби запису.

## Зміст

-   [ReflectionZendExtension::clone](reflectionzendextension.clone.md) - Обробник клонування
-   [ReflectionZendExtension::construct](reflectionzendextension.construct.md) - Конструктор
-   [ReflectionZendExtension::export](reflectionzendextension.export.md) - Експорт
-   [ReflectionZendExtension::getAuthor](reflectionzendextension.getauthor.md) — Отримує автора
-   [ReflectionZendExtension::getCopyright](reflectionzendextension.getcopyright.md) — Отримує авторські права
-   [ReflectionZendExtension::getName](reflectionzendextension.getname.md) — Отримує ім'я
-   [ReflectionZendExtension::getURL](reflectionzendextension.geturl.md) — Отримує URL
-   [ReflectionZendExtension::getVersion](reflectionzendextension.getversion.md) — Отримує версію
-   [ReflectionZendExtension::toString](reflectionzendextension.tostring.md) - Обробник перетворення в рядок
