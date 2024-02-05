---
navigation:
  - reflectionenum.isbacked.md: '« ReflectionEnum::isBacked'
  - reflectionenumunitcase.construct.md: 'ReflectionEnumUnitCase::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionEnumUnitCase
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionEnumUnitCase

(PHP 8 >= 8.1.0)

## Вступ

Класс**ReflectionEnumUnitCase** повідомляє інформацію про варіант перерахування, що не має скалярного еквівалента.

## Огляд класів

```classsynopsis

    
     class ReflectionEnumUnitCase
    

    
     extends
      ReflectionClassConstant
     {

    /* Наследуемые константы */
    
     public
     const
     int
      ReflectionClassConstant::IS_PUBLIC;
public
     const
     int
      ReflectionClassConstant::IS_PROTECTED;
public
     const
     int
      ReflectionClassConstant::IS_PRIVATE;
public
     const
     int
      ReflectionClassConstant::IS_FINAL;


    /* Наследуемые свойства */
    public
     string
      $name;
public
     string
      $class;


    /* Методы */
    
   public __construct(object|string $class, string $constant)

    public getEnum(): ReflectionEnum
public getValue(): UnitEnum


    /* Наследуемые методы */
    public static ReflectionClassConstant::export(mixed $class, string $name, bool $return = ?): string
public ReflectionClassConstant::getAttributes(?string $name = null, int $flags = 0): array
public ReflectionClassConstant::getDeclaringClass(): ReflectionClass
public ReflectionClassConstant::getDocComment(): string|false
public ReflectionClassConstant::getModifiers(): int
public ReflectionClassConstant::getName(): string
public ReflectionClassConstant::getValue(): mixed
public ReflectionClassConstant::isEnumCase(): bool
public ReflectionClassConstant::isFinal(): bool
public ReflectionClassConstant::isPrivate(): bool
public ReflectionClassConstant::isProtected(): bool
public ReflectionClassConstant::isPublic(): bool
public ReflectionClassConstant::__toString(): string

   }
```

## Дивіться також

-   [Перерахування](language.enumerations.md)
-   [ReflectionEnumBackedCase](class.reflectionenumbackedcase.md)

## Зміст

-   [ReflectionEnumUnitCase::\_\_construct](reflectionenumunitcase.construct.md)— Створює екземпляр об'єкту ReflectionEnumUnitCase
-   [ReflectionEnumUnitCase::getEnum](reflectionenumunitcase.getenum.md)— Отримує Reflection-об'єкт перерахування цього варіанта
-   [ReflectionEnumUnitCase::getValue](reflectionenumunitcase.getvalue.md)— Отримує об'єкт варіанта перерахування, описаний Reflection-об'єктом
