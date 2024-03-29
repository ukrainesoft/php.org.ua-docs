---
navigation:
  - reflectionnamedtype.isbuiltin.md: '« ReflectionNamedType::isBuiltin'
  - reflectionobject.construct.md: 'ReflectionObject::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionObject
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionObject

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**ReflectionObject** повідомляє інформацію про об'єкти (object).

## Огляд класів

```classsynopsis

    
     class ReflectionObject
    

    
     extends
      ReflectionClass
     {

    /* Наследуемые константы */
    
     public
     const
     int
      ReflectionClass::IS_IMPLICIT_ABSTRACT;
public
     const
     int
      ReflectionClass::IS_EXPLICIT_ABSTRACT;
public
     const
     int
      ReflectionClass::IS_FINAL;
public
     const
     int
      ReflectionClass::IS_READONLY;


    /* Наследуемые свойства */
    public
     string
      $name;


    /* Методы */
    
   public __construct(object $object)


    /* Наследуемые методы */
    public static ReflectionClass::export(mixed $argument, bool $return = false): string
public ReflectionClass::getAttributes(?string $name = null, int $flags = 0): array
public ReflectionClass::getConstant(string $name): mixed
public ReflectionClass::getConstants(?int $filter = null): array
public ReflectionClass::getConstructor(): ?ReflectionMethod
public ReflectionClass::getDefaultProperties(): array
public ReflectionClass::getDocComment(): string|false
public ReflectionClass::getEndLine(): int|false
public ReflectionClass::getExtension(): ?ReflectionExtension
public ReflectionClass::getExtensionName(): string|false
public ReflectionClass::getFileName(): string|false
public ReflectionClass::getInterfaceNames(): array
public ReflectionClass::getInterfaces(): array
public ReflectionClass::getMethod(string $name): ReflectionMethod
public ReflectionClass::getMethods(?int $filter = null): array
public ReflectionClass::getModifiers(): int
public ReflectionClass::getName(): string
public ReflectionClass::getNamespaceName(): string
public ReflectionClass::getParentClass(): ReflectionClass|false
public ReflectionClass::getProperties(?int $filter = null): array
public ReflectionClass::getProperty(string $name): ReflectionProperty
public ReflectionClass::getReflectionConstant(string $name): ReflectionClassConstant|false
public ReflectionClass::getReflectionConstants(?int $filter = null): array
public ReflectionClass::getShortName(): string
public ReflectionClass::getStartLine(): int|false
public ReflectionClass::getStaticProperties(): array
public ReflectionClass::getStaticPropertyValue(string $name, mixed &$def_value = ?): mixed
public ReflectionClass::getTraitAliases(): array
public ReflectionClass::getTraitNames(): array
public ReflectionClass::getTraits(): array
public ReflectionClass::hasConstant(string $name): bool
public ReflectionClass::hasMethod(string $name): bool
public ReflectionClass::hasProperty(string $name): bool
public ReflectionClass::implementsInterface(ReflectionClass|string $interface): bool
public ReflectionClass::inNamespace(): bool
public ReflectionClass::isAbstract(): bool
public ReflectionClass::isAnonymous(): bool
public ReflectionClass::isCloneable(): bool
public ReflectionClass::isEnum(): bool
public ReflectionClass::isFinal(): bool
public ReflectionClass::isInstance(object $object): bool
public ReflectionClass::isInstantiable(): bool
public ReflectionClass::isInterface(): bool
public ReflectionClass::isInternal(): bool
public ReflectionClass::isIterable(): bool
public ReflectionClass::isReadOnly(): bool
public ReflectionClass::isSubclassOf(ReflectionClass|string $class): bool
public ReflectionClass::isTrait(): bool
public ReflectionClass::isUserDefined(): bool
public ReflectionClass::newInstance(mixed ...$args): object
public ReflectionClass::newInstanceArgs(array $args = []): ?object
public ReflectionClass::newInstanceWithoutConstructor(): object
public ReflectionClass::setStaticPropertyValue(string $name, mixed $value): void
public ReflectionClass::__toString(): string

   }
```

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionObject::export()](reflectionobject.export.md)був видалений. |

## Зміст

-   [ReflectionObject::\_\_construct](reflectionobject.construct.md) \- Конструктор класу ReflectionObject
-   [ReflectionObject::export](reflectionobject.export.md) \- Експорт
