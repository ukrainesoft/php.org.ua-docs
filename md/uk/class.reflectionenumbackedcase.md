Клас ReflectionEnumBackedCase

-   [« ReflectionEnumUnitCase::getValue](reflectionenumunitcase.getvalue.html)
    
-   [ReflectionEnumBackedCase::\_\_construct »](reflectionenumbackedcase.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionEnumBackedCase
    

# Клас ReflectionEnumBackedCase

(PHP 8> = 8.1.0)

## Вступ

Клас **ReflectionEnumBackedCase** повідомляє інформацію про варіант типізованого перерахування, який має скалярний еквівалент.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionEnumBackedCase
     

     
      extends
       ReflectionEnumUnitCase
     
     {
    
    /* Наследуемые константы */
    
     const
     int
      ReflectionClassConstant::IS_PUBLIC = 1;
const
     int
      ReflectionClassConstant::IS_PROTECTED = 2;
const
     int
      ReflectionClassConstant::IS_PRIVATE = 4;


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

-   [Перечисления](language.enumerations.html)
-   [ReflectionEnumUnitCase](class.reflectionenumunitcase.html)

## Зміст

-   [ReflectionEnumBackedCase::\_\_construct](reflectionenumbackedcase.construct.html) — Створює об'єкт ReflectionEnumBackedCase
-   [ReflectionEnumBackedCase::getBackingValue](reflectionenumbackedcase.getbackingvalue.html) — Отримує скалярне значення варіанта перерахування