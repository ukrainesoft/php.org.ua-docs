---
navigation:
  - reflectionenumunitcase.getvalue.md: '« ReflectionEnumUnitCase::getValue'
  - reflectionenumbackedcase.construct.md: 'ReflectionEnumBackedCase::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionEnumBackedCase
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionEnumBackedCase

(PHP 8 >= 8.1.0)

## Вступ

Класс**ReflectionEnumBackedCase** повідомляє інформацію про варіант типізованого перерахування, який має скалярний еквівалент.

## Огляд класів

```classsynopsis

    
     class ReflectionEnumBackedCase
    

    
     extends
      ReflectionEnumUnitCase
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

    public getBackingValue(): int|string


    /* Наследуемые методы */
    public ReflectionEnumUnitCase::getEnum(): ReflectionEnum
public ReflectionEnumUnitCase::getValue(): UnitEnum

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
-   [ReflectionEnumUnitCase](class.reflectionenumunitcase.md)

## Зміст

-   [ReflectionEnumBackedCase::\_\_construct](reflectionenumbackedcase.construct.md)— Створює об'єкт ReflectionEnumBackedCase
-   [ReflectionEnumBackedCase::getBackingValue](reflectionenumbackedcase.getbackingvalue.md)— Отримує скалярне значення варіанта перерахування
