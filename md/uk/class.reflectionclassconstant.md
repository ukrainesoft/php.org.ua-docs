---
navigation:
  - reflectionclass.tostring.md: '« ReflectionClass::toString'
  - reflectionclassconstant.construct.md: 'ReflectionClassConstant::construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionClassConstant
---
# Клас ReflectionClassConstant

(PHP 7> = 7.1.0, PHP 8)

## Вступ

Клас **ReflectionClassConstant** використовується отримання інформації про константах класу.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionClassConstant
     

     implements 
       Reflector {
    /* Константы */
    
     const
     int
      IS_PUBLIC = 1;

    const
     int
      IS_PROTECTED = 2;

    const
     int
      IS_PRIVATE = 4;


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

> **Зауваження**
> 
> Ці константи можуть змінюватися від версії до версії PHP. Рекомендується завжди використовувати константи та не покладатися безпосередньо на значення.

## Зміст

-   [ReflectionClassConstant::construct](reflectionclassconstant.construct.md) — Створює ReflectionClassConstant
-   [ReflectionClassConstant::export](reflectionclassconstant.export.md) - Експорт
-   [ReflectionClassConstant::getAttributes](reflectionclassconstant.getattributes.md) — Отримує атрибути
-   [ReflectionClassConstant::getDeclaringClass](reflectionclassconstant.getdeclaringclass.md) — Отримує оголошуючий клас
-   [ReflectionClassConstant::getDocComment](reflectionclassconstant.getdoccomment.md) — Отримує doc-коментарі
-   [ReflectionClassConstant::getModifiers](reflectionclassconstant.getmodifiers.md) — Отримує модифікатори константи класу
-   [ReflectionClassConstant::getName](reflectionclassconstant.getname.md) — Отримати ім'я константи
-   [ReflectionClassConstant::getValue](reflectionclassconstant.getvalue.md) — Отримує значення
-   [ReflectionClassConstant::isEnumCase](reflectionclassconstant.isenumcase.md) — Перевіряє, чи є константа класу варіантом перерахування
-   [ReflectionClassConstant::isFinal](reflectionclassconstant.isfinal.md) — Перевіряє, чи константа класу є остаточною
-   [ReflectionClassConstant::isPrivate](reflectionclassconstant.isprivate.md) — Перевіряє, чи константа закрита
-   [ReflectionClassConstant::isProtected](reflectionclassconstant.isprotected.md) — Перевіряє, чи константа захищена
-   [ReflectionClassConstant::isPublic](reflectionclassconstant.ispublic.md) — Перевіряє, чи константа є загальнодоступною
-   [ReflectionClassConstant::toString](reflectionclassconstant.tostring.md) — Повертає строкове представлення об'єкта ReflectionClassConstant
