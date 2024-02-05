---
navigation:
  - reflectionfunctionabstract.tostring.md: '« ReflectionFunctionAbstract::\_\_function toString() { [native code] }'
  - reflectionmethod.construct.md: 'ReflectionMethod::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionMethod
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionMethod

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**ReflectionMethod** повідомляє інформацію про методи.

## Огляд класів

```classsynopsis

    
     class ReflectionMethod
    

    
     extends
      ReflectionFunctionAbstract
     {


    /* Константы */
    
     public
     const
     int
      IS_STATIC;

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
      IS_ABSTRACT;

    public
     const
     int
      IS_FINAL;


    /* Свойства */
    public
     string
      $class;


    /* Наследуемые свойства */
    public
     string
      $name;


    /* Методы */
    
   public __construct(object|string $objectOrMethod, string $method)
public __construct(string $classMethod)

    public static createFromMethodName(string $method): static
public static export(string $class, string $name, bool $return = false): string
public getClosure(?object $object = null): Closure
public getDeclaringClass(): ReflectionClass
public getModifiers(): int
public getPrototype(): ReflectionMethod
public hasPrototype(): bool
public invoke(?object $object, mixed ...$args): mixed
public invokeArgs(?object $object, array $args): mixed
public isAbstract(): bool
public isConstructor(): bool
public isDestructor(): bool
public isFinal(): bool
public isPrivate(): bool
public isProtected(): bool
public isPublic(): bool
public setAccessible(bool $accessible): void
public __toString(): string


    /* Наследуемые методы */
    private ReflectionFunctionAbstract::__clone(): void
public ReflectionFunctionAbstract::getAttributes(?string $name = null, int $flags = 0): array
public ReflectionFunctionAbstract::getClosureScopeClass(): ?ReflectionClass
public ReflectionFunctionAbstract::getClosureThis(): ?object
public ReflectionFunctionAbstract::getClosureUsedVariables(): array
public ReflectionFunctionAbstract::getDocComment(): string|false
public ReflectionFunctionAbstract::getEndLine(): int|false
public ReflectionFunctionAbstract::getExtension(): ?ReflectionExtension
public ReflectionFunctionAbstract::getExtensionName(): string|false
public ReflectionFunctionAbstract::getFileName(): string|false
public ReflectionFunctionAbstract::getName(): string
public ReflectionFunctionAbstract::getNamespaceName(): string
public ReflectionFunctionAbstract::getNumberOfParameters(): int
public ReflectionFunctionAbstract::getNumberOfRequiredParameters(): int
public ReflectionFunctionAbstract::getParameters(): array
public ReflectionFunctionAbstract::getReturnType(): ?ReflectionType
public ReflectionFunctionAbstract::getShortName(): string
public ReflectionFunctionAbstract::getStartLine(): int|false
public ReflectionFunctionAbstract::getStaticVariables(): array
public ReflectionFunctionAbstract::getTentativeReturnType(): ?ReflectionType
public ReflectionFunctionAbstract::hasReturnType(): bool
public ReflectionFunctionAbstract::hasTentativeReturnType(): bool
public ReflectionFunctionAbstract::inNamespace(): bool
public ReflectionFunctionAbstract::isClosure(): bool
public ReflectionFunctionAbstract::isDeprecated(): bool
public ReflectionFunctionAbstract::isGenerator(): bool
public ReflectionFunctionAbstract::isInternal(): bool
public ReflectionFunctionAbstract::isStatic(): bool
public ReflectionFunctionAbstract::isUserDefined(): bool
public ReflectionFunctionAbstract::isVariadic(): bool
public ReflectionFunctionAbstract::returnsReference(): bool
abstract public ReflectionFunctionAbstract::__toString(): void

   }
```

## Властивості

name

Ім'я методу

class

Ім'я класу

## Обумовлені константи

## Модифікатори ReflectionMethod

**`ReflectionMethod::IS_STATIC`**

Вказує, що це статичний метод. До PHP 7.4.0, значення було

**`ReflectionMethod::IS_PUBLIC`**

Вказує, що це загальнодоступний метод. До PHP 7.4.0, значення було `256`

**`ReflectionMethod::IS_PROTECTED`**

Вказує, що це захищений метод. До PHP 7.4.0, значення було `512`

**`ReflectionMethod::IS_PRIVATE`**

Вказує, що це закритий метод. До PHP 7.4.0, значення було `1024`

**`ReflectionMethod::IS_ABSTRACT`**

Вказує, що це абстрактний метод. До PHP 7.4.0, значення було

**`ReflectionMethod::IS_FINAL`**

Вказує, що це остаточний метод. До PHP 7.4.0, значення було `4`

> **Зауваження** :
> 
> Ці константи можуть змінюватися від версії до версії PHP. Рекомендується завжди використовувати константи і не покладатися безпосередньо на значення.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionMethod::export()](reflectionmethod.export.md)був видалений. |

## Зміст

-   [ReflectionMethod::\_\_construct](reflectionmethod.construct.md) \- Конструктор класу ReflectionMethod
-   [ReflectionMethod::createFromMethodName](reflectionmethod.createfrommethodname.md)— Створює об'єкт класу ReflectionMethod
-   [ReflectionMethod::export](reflectionmethod.export.md) \- Експорт відбитого методу
-   [ReflectionMethod::getClosure](reflectionmethod.getclosure.md)— Повертає динамічно створене замикання для методу
-   [ReflectionMethod::getDeclaringClass](reflectionmethod.getdeclaringclass.md)— Отримує клас, що оголошує відбитий метод
-   [ReflectionMethod::getModifiers](reflectionmethod.getmodifiers.md)— Отримує модифікатори методу
-   [ReflectionMethod::getPrototype](reflectionmethod.getprototype.md)— Отримує прототип методу (якщо такий є)
-   [ReflectionMethod::hasPrototype](reflectionmethod.hasprototype.md)— Визначає, чи має метод прототип
-   [ReflectionMethod::invoke](reflectionmethod.invoke.md) \- Виклик
-   [ReflectionMethod::invokeArgs](reflectionmethod.invokeargs.md) \- Виклик методу з передачею аргументів масивом
-   [ReflectionMethod::isAbstract](reflectionmethod.isabstract.md)— Перевіряє, чи є метод абстрактним
-   [ReflectionMethod::isConstructor](reflectionmethod.isconstructor.md)— Перевіряє, чи є метод конструктором
-   [ReflectionMethod::isDestructor](reflectionmethod.isdestructor.md)— Перевіряє, чи є метод деструктором
-   [ReflectionMethod::isFinal](reflectionmethod.isfinal.md)— Перевіряє, чи є метод остаточним
-   [ReflectionMethod::isPrivate](reflectionmethod.isprivate.md)— Перевіряє, чи є метод закритим
-   [ReflectionMethod::isProtected](reflectionmethod.isprotected.md)— Перевіряє, чи метод захищений
-   [ReflectionMethod::isPublic](reflectionmethod.ispublic.md)— Перевіряє, чи є метод загальнодоступним
-   [ReflectionMethod::setAccessible](reflectionmethod.setaccessible.md)— Робить метод доступним
-   [ReflectionMethod::\_\_function toString() { \[native code\] }](reflectionmethod.tostring.md)— Повертає рядкову виставу об'єкта ReflectionMethod
