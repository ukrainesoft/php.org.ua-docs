---
navigation:
  - reflectionzendextension.tostring.md: '« ReflectionZendExtension::\_\_function toString() { [native code] }'
  - reflectionextension.clone.md: 'ReflectionExtension::\_\_clone »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionExtension
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionExtension

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**ReflectionExtension** повідомляє інформацію про модулі.

## Огляд класів

```classsynopsis

    
     class ReflectionExtension
    

    
     implements
      Reflector {

    /* Свойства */
    
     public
     string
      $name;


    /* Методы */
    
   public __construct(string $name)

    private __clone(): void
public static export(string $name, string $return = false): string
public getClasses(): array
public getClassNames(): array
public getConstants(): array
public getDependencies(): array
public getFunctions(): array
public getINIEntries(): array
public getName(): string
public getVersion(): ?string
public info(): void
public isPersistent(): bool
public isTemporary(): bool
public __toString(): string

   }
```

## Властивості

name

Ім'я модуль. Значення властивості збігається з тим, що метод повертає метод [ReflectionExtension::getName()](reflectionextension.getname.md)

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionExtension::export()](reflectionextension.export.md)був видалений. |

## Зміст

-   [ReflectionExtension::\_\_clone](reflectionextension.clone.md) \- Клонує об'єкт
-   [ReflectionExtension::\_\_construct](reflectionextension.construct.md)— Створює об'єкт класу ReflectionExtension
-   [ReflectionExtension::export](reflectionextension.export.md) \- Експортує модуль
-   [ReflectionExtension::getClasses](reflectionextension.getclasses.md) \- Повертає класи
-   [ReflectionExtension::getClassNames](reflectionextension.getclassnames.md) \- Отримання імен класів
-   [ReflectionExtension::getConstants](reflectionextension.getconstants.md) \- Отримання констант
-   [ReflectionExtension::getDependencies](reflectionextension.getdependencies.md) \- Отримання залежностей
-   [ReflectionExtension::getFunctions](reflectionextension.getfunctions.md)— Отримання функцій модуля
-   [ReflectionExtension::getINIEntries](reflectionextension.getinientries.md)— Отримання ini-налаштувань модуля
-   [ReflectionExtension::getName](reflectionextension.getname.md)— Отримання імені модуля
-   [ReflectionExtension::getVersion](reflectionextension.getversion.md)— Отримання версії модуля
-   [ReflectionExtension::info](reflectionextension.info.md)— Виведення інформації про модуль
-   [ReflectionExtension::isPersistent](reflectionextension.ispersistent.md)— Визначає, чи модуль є постійним
-   [ReflectionExtension::isTemporary](reflectionextension.istemporary.md)— Визначає, чи модуль є тимчасовим
-   [ReflectionExtension::\_\_function toString() { \[native code\] }](reflectionextension.tostring.md)— Перетворення на рядок
