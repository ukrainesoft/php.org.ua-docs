Клас ReflectionFunction

-   [« ReflectionExtension::\_\_toString](reflectionextension.tostring.html)
    
-   [ReflectionFunction::\_\_construct »](reflectionfunction.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionFunction
    

# Клас ReflectionFunction

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **ReflectionFunction** повідомляє інформацію про функції.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionFunction
     

     
      extends
       ReflectionFunctionAbstract
     
     {

    /* Константы */
    
     const
     int
      IS_DEPRECATED = 262144;


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

## Зміст

-   [ReflectionFunction::\_\_construct](reflectionfunction.construct.html) - Конструктор класу ReflectionFunction
-   [ReflectionFunction::export](reflectionfunction.export.html) - Експортує функції
-   [ReflectionFunction::getClosure](reflectionfunction.getclosure.html) — Повертає динамічно створене замикання функції
-   [ReflectionFunction::invoke](reflectionfunction.invoke.html) - Викликає функцію
-   [ReflectionFunction::invokeArgs](reflectionfunction.invokeargs.html) - Виклик функції з передачею аргументів
-   [ReflectionFunction::isDisabled](reflectionfunction.isdisabled.html) — Перевіряє, що функцію вимкнено
-   [ReflectionFunction::\_\_toString](reflectionfunction.tostring.html) — Подання у вигляді рядка