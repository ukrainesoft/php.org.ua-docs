---
navigation:
  - reflectionextension.tostring.md: '« ReflectionExtension::\_\_function toString() { [native code] }'
  - reflectionfunction.construct.md: 'ReflectionFunction::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionFunction
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionFunction

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**ReflectionFunction** повідомляє інформацію про функції.

## Огляд класів

```classsynopsis

    
     class ReflectionFunction
    

    
     extends
      ReflectionFunctionAbstract
     {

    /* Константы */
    
     public
     const
     int
      IS_DEPRECATED;


    /* Наследуемые свойства */
    public
     string
      $name;


    /* Методы */
    
   public __construct(Closure|string $function)

    public static export(string $name, string $return = ?): string
public getClosure(): Closure
public invoke(mixed ...$args): mixed
public invokeArgs(array $args): mixed
public isAnonymous(): bool
public isDisabled(): bool
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

## Обумовлені константи

## Модифікатори ReflectionFunction

**`ReflectionFunction::IS_DEPRECATED`**

Вказує, що функція застаріла (deprecated).

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionFunction::export()](reflectionfunction.export.md)був видалений. |

## Зміст

-   [ReflectionFunction::\_\_construct](reflectionfunction.construct.md) \- Конструктор класу ReflectionFunction
-   [ReflectionFunction::export](reflectionfunction.export.md) \- Експортує функції
-   [ReflectionFunction::getClosure](reflectionfunction.getclosure.md)— Повертає динамічно створене замикання функції
-   [ReflectionFunction::invoke](reflectionfunction.invoke.md) \- Викликає функцію
-   [ReflectionFunction::invokeArgs](reflectionfunction.invokeargs.md) \- Виклик функції з передачею аргументів
-   [ReflectionFunction::isAnonymous](reflectionfunction.isanonymous.md)— Перевіряє, чи є функція анонімною
-   [ReflectionFunction::isDisabled](reflectionfunction.isdisabled.md)— Перевіряє, що функцію вимкнено
-   [ReflectionFunction::\_\_function toString() { \[native code\] }](reflectionfunction.tostring.md)— Повертає рядкову виставу об'єкта ReflectionFunction
