---
navigation:
  - reflection.getmodifiernames.md: '« Reflection::getModifierNames'
  - reflectionclass.construct.md: 'ReflectionClass::\_\_construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionClass
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionClass

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**ReflectionClass**сообщает информацию о классе.

## Огляд класів

```classsynopsis

    
     class ReflectionClass
    

    
     implements
      Reflector {

    /* Константы */
    
     public
     const
     int
      IS_IMPLICIT_ABSTRACT;

    public
     const
     int
      IS_EXPLICIT_ABSTRACT;

    public
     const
     int
      IS_FINAL;

    public
     const
     int
      IS_READONLY;


    /* Свойства */
    public
     string
      $name;


    /* Методы */
    
   public __construct(object|string $objectOrClass)

    public static export(mixed $argument, bool $return = false): string
public getAttributes(?string $name = null, int $flags = 0): array
public getConstant(string $name): mixed
public getConstants(?int $filter = null): array
public getConstructor(): ?ReflectionMethod
public getDefaultProperties(): array
public getDocComment(): string|false
public getEndLine(): int|false
public getExtension(): ?ReflectionExtension
public getExtensionName(): string|false
public getFileName(): string|false
public getInterfaceNames(): array
public getInterfaces(): array
public getMethod(string $name): ReflectionMethod
public getMethods(?int $filter = null): array
public getModifiers(): int
public getName(): string
public getNamespaceName(): string
public getParentClass(): ReflectionClass|false
public getProperties(?int $filter = null): array
public getProperty(string $name): ReflectionProperty
public getReflectionConstant(string $name): ReflectionClassConstant|false
public getReflectionConstants(?int $filter = null): array
public getShortName(): string
public getStartLine(): int|false
public getStaticProperties(): array
public getStaticPropertyValue(string $name, mixed &$def_value = ?): mixed
public getTraitAliases(): array
public getTraitNames(): array
public getTraits(): array
public hasConstant(string $name): bool
public hasMethod(string $name): bool
public hasProperty(string $name): bool
public implementsInterface(ReflectionClass|string $interface): bool
public inNamespace(): bool
public isAbstract(): bool
public isAnonymous(): bool
public isCloneable(): bool
public isEnum(): bool
public isFinal(): bool
public isInstance(object $object): bool
public isInstantiable(): bool
public isInterface(): bool
public isInternal(): bool
public isIterable(): bool
public isReadOnly(): bool
public isSubclassOf(ReflectionClass|string $class): bool
public isTrait(): bool
public isUserDefined(): bool
public newInstance(mixed ...$args): object
public newInstanceArgs(array $args = []): ?object
public newInstanceWithoutConstructor(): object
public setStaticPropertyValue(string $name, mixed $value): void
public __toString(): string

   }
```

## Властивості

name

Назва класу. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.md) під час спроби запису.

## Обумовлені константи

## Модифікатори ReflectionClass

**`ReflectionClass::IS_IMPLICIT_ABSTRACT`**

Вказує, що клас є [абстрактним](language.oop5.abstract.md)тому, що він містить абстрактні методи.

**`ReflectionClass::IS_EXPLICIT_ABSTRACT`**

Вказує, що клас є [абстрактним](language.oop5.abstract.md)тому що так зазначено при його описі.

**`ReflectionClass::IS_FINAL`**

Вказує, що клас є [остаточним (final)](language.oop5.final.md)

**`ReflectionClass::IS_READONLY`**

Вказує, що клас є [readonly](language.oop5.basic.md#language.oop5.basic.class.readonly)

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionClass::export()](reflectionclass.export.md)був видалений. |

## Зміст

-   [ReflectionClass::\_\_construct](reflectionclass.construct.md)— Створює об'єкт класу ReflectionClass
-   [ReflectionClass::export](reflectionclass.export.md) \- Експортує клас
-   [ReflectionClass::getAttributes](reflectionclass.getattributes.md)— Отримує атрибути
-   [ReflectionClass::getConstant](reflectionclass.getconstant.md)— Повертає певну константу
-   [ReflectionClass::getConstants](reflectionclass.getconstants.md)— Повертає константи
-   [ReflectionClass::getConstructor](reflectionclass.getconstructor.md) \- Повертає конструктор класу
-   [ReflectionClass::getDefaultProperties](reflectionclass.getdefaultproperties.md)— Повертає властивості за промовчанням
-   [ReflectionClass::getDocComment](reflectionclass.getdoccomment.md)— Повертає doc-блоки коментарів
-   [ReflectionClass::getEndLine](reflectionclass.getendline.md)— Повертає номер останнього рядка
-   [ReflectionClass::getExtension](reflectionclass.getextension.md)— Повертає об'єкт класу ReflectionExtension для модуля, що визначає клас
-   [ReflectionClass::getExtensionName](reflectionclass.getextensionname.md) \- Повертає ім'я модуля, що визначає клас
-   [ReflectionClass::getFileName](reflectionclass.getfilename.md)— Повертає ім'я файлу, у якому визначено клас
-   [ReflectionClass::getInterfaceNames](reflectionclass.getinterfacenames.md)— Повертає імена інтерфейсів
-   [ReflectionClass::getInterfaces](reflectionclass.getinterfaces.md)— Повертає інтерфейси
-   [ReflectionClass::getMethod](reflectionclass.getmethod.md)— Повертає екземпляр ReflectionMethod для методу класу
-   [ReflectionClass::getMethods](reflectionclass.getmethods.md)— Повертає список методів у вигляді масиву
-   [ReflectionClass::getModifiers](reflectionclass.getmodifiers.md)— Повертає інформацію про модифікаторів класу
-   [ReflectionClass::getName](reflectionclass.getname.md) \- Повертає ім'я класу
-   [ReflectionClass::getNamespaceName](reflectionclass.getnamespacename.md)— Повертає назву простору імен
-   [ReflectionClass::getParentClass](reflectionclass.getparentclass.md) \- Повертає батьківський клас
-   [ReflectionClass::getProperties](reflectionclass.getproperties.md) \- Повертає властивості
-   [ReflectionClass::getProperty](reflectionclass.getproperty.md)— Повертає екземпляр ReflectionProperty для якості класу
-   [ReflectionClass::getReflectionConstant](reflectionclass.getreflectionconstant.md)— Отримує ReflectionClassConstant для константи класу
-   [ReflectionClass::getReflectionConstants](reflectionclass.getreflectionconstants.md)— Отримує константи класу
-   [ReflectionClass::getShortName](reflectionclass.getshortname.md) \- Повертає коротке ім'я
-   [ReflectionClass::getStartLine](reflectionclass.getstartline.md)— Повертає номер початкового рядка
-   [ReflectionClass::getStaticProperties](reflectionclass.getstaticproperties.md)— Повертає статичні властивості
-   [ReflectionClass::getStaticPropertyValue](reflectionclass.getstaticpropertyvalue.md)— Повертає значення статичної властивості
-   [ReflectionClass::getTraitAliases](reflectionclass.gettraitaliases.md)— Повертає масив псевдонімів трейтів
-   [ReflectionClass::getTraitNames](reflectionclass.gettraitnames.md)— Повертає масив імен трейтів, які використовуються у цьому класі
-   [ReflectionClass::getTraits](reflectionclass.gettraits.md)— Повертає масив трейтів, які використовуються у цьому класі.
-   [ReflectionClass::hasConstant](reflectionclass.hasconstant.md)— Перевіряє, чи визначено константу
-   [ReflectionClass::hasMethod](reflectionclass.hasmethod.md)— Перевіряє, чи заданий метод
-   [ReflectionClass::hasProperty](reflectionclass.hasproperty.md)— Перевіряє, чи визначено властивість
-   [ReflectionClass::implementsInterface](reflectionclass.implementsinterface.md)— Перевіряє, чи реалізується інтерфейс
-   [ReflectionClass::inNamespace](reflectionclass.innamespace.md)— Перевіряє, чи визначений клас у просторі імен
-   [ReflectionClass::isAbstract](reflectionclass.isabstract.md)— Перевіряє, чи клас є абстрактним.
-   [ReflectionClass::isAnonymous](reflectionclass.isanonymous.md)— Перевіряє, чи є клас анонімним
-   [ReflectionClass::isCloneable](reflectionclass.iscloneable.md)— Перевіряє, чи можна клонувати цей клас
-   [ReflectionClass::isEnum](reflectionclass.isenum.md)— Повертає, чи є клас перерахуванням
-   [ReflectionClass::isFinal](reflectionclass.isfinal.md)— Перевіряє, чи клас остаточний (final)
-   [ReflectionClass::isInstance](reflectionclass.isinstance.md)— Перевіряє, чи об'єкт належить класу
-   [ReflectionClass::isInstantiable](reflectionclass.isinstantiable.md)— Перевіряє, чи можна створити екземпляр класу
-   [ReflectionClass::isInterface](reflectionclass.isinterface.md)— Перевіряє, чи клас є інтерфейсом
-   [ReflectionClass::isInternal](reflectionclass.isinternal.md)— Перевіряє, чи є клас вбудованим у модуль чи ядро
-   [ReflectionClass::isIterable](reflectionclass.isiterable.md)— Перевірити, чи клас ітерується.
-   [ReflectionClass::isIterateable](reflectionclass.isiterateable.md) \- Псевдонім ReflectionClass::isIterable
-   [ReflectionClass::isReadOnly](reflectionclass.isreadonly.md)— Перевіряє, чи є клас доступним лише для читання
-   [ReflectionClass::isSubclassOf](reflectionclass.issubclassof.md)— Перевіряє, чи є клас підкласом
-   [ReflectionClass::isTrait](reflectionclass.istrait.md)— Перевіряє, чи це є трейтом.
-   [ReflectionClass::isUserDefined](reflectionclass.isuserdefined.md)— Перевіряє, чи є клас для користувача
-   [ReflectionClass::newInstance](reflectionclass.newinstance.md) \- Створює екземпляр класу з переданими аргументами
-   [ReflectionClass::newInstanceArgs](reflectionclass.newinstanceargs.md) \- Створює екземпляр класу з переданими параметрами
-   [ReflectionClass::newInstanceWithoutConstructor](reflectionclass.newinstancewithoutconstructor.md) \- Створює новий екземпляр класу без виклику конструктора
-   [ReflectionClass::setStaticPropertyValue](reflectionclass.setstaticpropertyvalue.md) \- Встановлює значення статичної властивості
-   [ReflectionClass::\_\_function toString() { \[native code\] }](reflectionclass.tostring.md)— Повертає рядкову виставу об'єкта класу ReflectionClass
