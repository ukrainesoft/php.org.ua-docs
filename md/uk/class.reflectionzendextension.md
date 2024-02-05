---
navigation:
  - reflectionenumbackedcase.getbackingvalue.md: '« ReflectionEnumBackedCase::getBackingValue'
  - reflectionzendextension.clone.md: 'ReflectionZendExtension::\_\_clone »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionZendExtension
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionZendExtension

(PHP 5 >= 5.4.0, PHP 7, PHP 8)

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

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionZendExtension::export()](reflectionzendextension.export.md)був видалений. |

## Зміст

-   [ReflectionZendExtension::\_\_clone](reflectionzendextension.clone.md) \- Обробник клонування
-   [ReflectionZendExtension::\_\_construct](reflectionzendextension.construct.md)— Створює об'єкт ReflectionZendExtension
-   [ReflectionZendExtension::export](reflectionzendextension.export.md) \- Експорт
-   [ReflectionZendExtension::getAuthor](reflectionzendextension.getauthor.md)— Отримує автора
-   [ReflectionZendExtension::getCopyright](reflectionzendextension.getcopyright.md)— Отримує авторські права
-   [ReflectionZendExtension::getName](reflectionzendextension.getname.md)— Отримує ім'я
-   [ReflectionZendExtension::getURL](reflectionzendextension.geturl.md)— Отримує URL
-   [ReflectionZendExtension::getVersion](reflectionzendextension.getversion.md)— Отримує версію
-   [ReflectionZendExtension::\_\_function toString() { \[native code\] }](reflectionzendextension.tostring.md) \- Обробник перетворення в рядок
