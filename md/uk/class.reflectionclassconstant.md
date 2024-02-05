---
navigation:
  - reflectionclass.tostring.md: '« ReflectionClass::\_\_function toString() { [native code] }'
  - reflectionclassconstant.construct.md: 'ReflectionClassConstant::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionClassConstant
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionClassConstant

(PHP 7 >= 7.1.0, PHP 8)

## Вступ

Класс**ReflectionClassConstant** використовується отримання інформації про константах класу.

## Огляд класів

```classsynopsis

    
     class ReflectionClassConstant
    

    
     implements
      Reflector {

    /* Константы */
    
     public
     const
     int
      IS_PUBLIC;

    public
     const
     int
      IS_PROTECTED;

    public
     const
     int
      IS_PRIVATE;

    public
     const
     int
      IS_FINAL;


    /* Свойства */
    public
     string
      $name;

    public
     string
      $class;


    /* Методы */
    
   public __construct(object|string $class, string $constant)

    public static export(mixed $class, string $name, bool $return = ?): string
public getAttributes(?string $name = null, int $flags = 0): array
public getDeclaringClass(): ReflectionClass
public getDocComment(): string|false
public getModifiers(): int
public getName(): string
public getValue(): mixed
public isEnumCase(): bool
public isFinal(): bool
public isPrivate(): bool
public isProtected(): bool
public isPublic(): bool
public __toString(): string

   }
```

## Властивості

name

Ім'я константи класу. Лише читання. У разі спроби зміни викидає виняток [ReflectionException](class.reflectionexception.md)

class

Ім'я класу, у якому визначено константу. Лише читання. У разі спроби зміни викидає виняток [ReflectionException](class.reflectionexception.md)

## Обумовлені константи

## ReflectionClassConstant Modifiers

**`ReflectionClassConstant::IS_PUBLIC`**

Вказує, що константа є [загальнодоступною](language.oop5.visibility.md). До PHP 7.4.0, значення було `256`

**`ReflectionClassConstant::IS_PROTECTED`**

Вказує, що константа є [захищеною](language.oop5.visibility.md). До PHP 7.4.0, значення було `512`

**`ReflectionClassConstant::IS_PRIVATE`**

Вказує, що константа є [закритою](language.oop5.visibility.md). До PHP 7.4.0, значення було `1024`

**`ReflectionClassConstant::IS_FINAL`**

Вказує, що константа є остаточною [final](language.oop5.final.md). Доступно з PHP 8.1.0.

> **Зауваження** :
> 
> Ці константи можуть змінюватися від версії до версії PHP. Рекомендується завжди використовувати константи і не покладатися безпосередньо на значення.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionClassConstant::export()](reflectionclassconstant.export.md)був видалений. |

## Зміст

-   [ReflectionClassConstant::\_\_construct](reflectionclassconstant.construct.md)— Створює об'єкт ReflectionClassConstant
-   [ReflectionClassConstant::export](reflectionclassconstant.export.md) \- Експорт
-   [ReflectionClassConstant::getAttributes](reflectionclassconstant.getattributes.md)— Отримує атрибути
-   [ReflectionClassConstant::getDeclaringClass](reflectionclassconstant.getdeclaringclass.md)— Отримує оголошуючий клас
-   [ReflectionClassConstant::getDocComment](reflectionclassconstant.getdoccomment.md)— Отримує doc-коментарі
-   [ReflectionClassConstant::getModifiers](reflectionclassconstant.getmodifiers.md)— Отримує модифікатори константи класу
-   [ReflectionClassConstant::getName](reflectionclassconstant.getname.md)— Отримати ім'я константи
-   [ReflectionClassConstant::getValue](reflectionclassconstant.getvalue.md)— Отримує значення
-   [ReflectionClassConstant::isEnumCase](reflectionclassconstant.isenumcase.md)— Перевіряє, чи константа класу є варіантом перерахування
-   [ReflectionClassConstant::isFinal](reflectionclassconstant.isfinal.md)— Перевіряє, чи константа класу є остаточною
-   [ReflectionClassConstant::isPrivate](reflectionclassconstant.isprivate.md)— Перевіряє, чи константа закрита
-   [ReflectionClassConstant::isProtected](reflectionclassconstant.isprotected.md)— Перевіряє, чи константа захищена
-   [ReflectionClassConstant::isPublic](reflectionclassconstant.ispublic.md)— Перевіряє, чи константа є загальнодоступною
-   [ReflectionClassConstant::\_\_function toString() { \[native code\] }](reflectionclassconstant.tostring.md)— Повертає строкове представлення об'єкта ReflectionClassConstant
