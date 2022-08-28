Клас ReflectionMethod

-   [« ReflectionFunctionAbstract::\_\_toString](reflectionfunctionabstract.tostring.html)
    
-   [ReflectionMethod::\_\_construct »](reflectionmethod.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionMethod
    

# Клас ReflectionMethod

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **ReflectionMethod** повідомляє інформацію про методи.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionMethod
     

     
      extends
       ReflectionFunctionAbstract
     
     {

    /* Константы */
    
     const
     int
      IS_STATIC = 16;

    const
     int
      IS_PUBLIC = 1;

    const
     int
      IS_PROTECTED = 2;

    const
     int
      IS_PRIVATE = 4;

    const
     int
      IS_ABSTRACT = 64;

    const
     int
      IS_FINAL = 32;


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

    public static export(string $class, string $name, bool $return = false): string
public getClosure(?object $object = null): Closure
public getDeclaringClass(): ReflectionClass
public getModifiers(): int
public getPrototype(): ReflectionMethod
public invoke(?object $object, mixed ...$args): mixed
public invokeArgs(?object $object, array $args): mixed
public isAbstract(): bool
public isConstructor(): bool
public isDestructor(): bool
public isFinal(): bool
public isPrivate(): bool
public isProtected(): bool
public isPublic(): bool
public isStatic(): bool
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

Вказує, що це статичний метод. До PHP 7.4.0, значення було `1`

**`ReflectionMethod::IS_PUBLIC`**

Вказує, що це загальнодоступний метод. До PHP 7.4.0, значення було `256`

**`ReflectionMethod::IS_PROTECTED`**

Вказує, що це захищений метод. До PHP 7.4.0, значення було `512`

**`ReflectionMethod::IS_PRIVATE`**

Вказує, що це закритий метод. До PHP 7.4.0, значення було `1024`

**`ReflectionMethod::IS_ABSTRACT`**

Вказує, що це абстрактний метод. До PHP 7.4.0, значення було `2`

**`ReflectionMethod::IS_FINAL`**

Вказує, що це остаточний метод. До PHP 7.4.0, значення було `4`

> **Зауваження**
> 
> Ці константи можуть змінюватися від версії до версії PHP. Рекомендується завжди використовувати константи та не покладатися безпосередньо на значення.

## Зміст

-   [ReflectionMethod::\_\_construct](reflectionmethod.construct.html) - Конструктор класу ReflectionMethod
-   [ReflectionMethod::export](reflectionmethod.export.html) - Експорт відбитого методу
-   [ReflectionMethod::getClosure](reflectionmethod.getclosure.html) — Повертає динамічно створене замикання для методу
-   [ReflectionMethod::getDeclaringClass](reflectionmethod.getdeclaringclass.html) — Отримує клас, що оголошує відбитий метод
-   [ReflectionMethod::getModifiers](reflectionmethod.getmodifiers.html) — Отримує модифікатори методу
-   [ReflectionMethod::getPrototype](reflectionmethod.getprototype.html) — Отримує прототип методу (якщо такий є)
-   [ReflectionMethod::invoke](reflectionmethod.invoke.html) - Виклик
-   [ReflectionMethod::invokeArgs](reflectionmethod.invokeargs.html) - Виклик методу з передачею аргументів масивом
-   [ReflectionMethod::isAbstract](reflectionmethod.isabstract.html) — Перевіряє, чи є метод абстрактним
-   [ReflectionMethod::isConstructor](reflectionmethod.isconstructor.html) — Перевіряє, чи є метод конструктором
-   [ReflectionMethod::isDestructor](reflectionmethod.isdestructor.html) — Перевіряє, чи є метод деструктором
-   [ReflectionMethod::isFinal](reflectionmethod.isfinal.html) — Перевіряє, чи є метод остаточним
-   [ReflectionMethod::isPrivate](reflectionmethod.isprivate.html) — Перевіряє, чи є метод закритим
-   [ReflectionMethod::isProtected](reflectionmethod.isprotected.html) — Перевіряє, чи метод захищений
-   [ReflectionMethod::isPublic](reflectionmethod.ispublic.html) — Перевіряє, чи є метод загальнодоступним
-   [ReflectionMethod::isStatic](reflectionmethod.isstatic.html) — Перевіряє, чи метод статичний
-   [ReflectionMethod::setAccessible](reflectionmethod.setaccessible.html) — Робить метод доступним
-   [ReflectionMethod::\_\_toString](reflectionmethod.tostring.html) — Повертає рядкову виставу об'єкта ReflectionMethod