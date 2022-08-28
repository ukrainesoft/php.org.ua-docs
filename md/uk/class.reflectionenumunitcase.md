Клас ReflectionEnumUnitCase

-   [« ReflectionEnum::isBacked](reflectionenum.isbacked.html)
    
-   [ReflectionEnumUnitCase::\_\_construct »](reflectionenumunitcase.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionEnumUnitCase
    

# Клас ReflectionEnumUnitCase

(PHP 8> = 8.1.0)

## Вступ

Клас **ReflectionEnumUnitCase** повідомляє інформацію про варіант перерахування, що не має скалярного еквівалента.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionEnumUnitCase
     

     
      extends
       ReflectionClassConstant
     
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

-   [Перечисления](language.enumerations.html)
-   [ReflectionEnumBackedCase](class.reflectionenumbackedcase.html)

## Зміст

-   [ReflectionEnumUnitCase::\_\_construct](reflectionenumunitcase.construct.html) — Створює екземпляр об'єкту ReflectionEnumUnitCase
-   [ReflectionEnumUnitCase::getEnum](reflectionenumunitcase.getenum.html) — Отримує Reflection-об'єкт перерахування цього варіанта
-   [ReflectionEnumUnitCase::getValue](reflectionenumunitcase.getvalue.html) — Отримує об'єкт варіанта перерахування, описаний Reflection-об'єктом