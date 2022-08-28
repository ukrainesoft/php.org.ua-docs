Клас ReflectionClass

-   [« Reflection::getModifierNames](reflection.getmodifiernames.html)
    
-   [ReflectionClass::\_\_construct »](reflectionclass.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionClass
    

# Клас ReflectionClass

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **ReflectionClass** повідомляє інформацію про клас.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionClass
     

     implements 
       Reflector {
    /* Константы */
    
     const
     int
      IS_IMPLICIT_ABSTRACT = 16;

    const
     int
      IS_EXPLICIT_ABSTRACT = 32;

    const
     int
      IS_FINAL = 64;


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
public getStaticProperties(): ?array
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

Назва класу. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.html) під час спроби запису.

## Обумовлені константи

## Модифікатори ReflectionClass

**`ReflectionClass::IS_IMPLICIT_ABSTRACT`**

Вказує, що клас є [абстрактным](language.oop5.abstract.html)тому, що він містить абстрактні методи.

**`ReflectionClass::IS_EXPLICIT_ABSTRACT`**

Вказує, що клас є [абстрактным](language.oop5.abstract.html)тому що так зазначено при його описі.

**`ReflectionClass::IS_FINAL`**

Вказує, що клас є [окончательным (final)](language.oop5.final.html)

## Зміст

-   [ReflectionClass::\_\_construct](reflectionclass.construct.html) — Створює об'єкт класу ReflectionClass
-   [ReflectionClass::export](reflectionclass.export.html) - Експортує клас
-   [ReflectionClass::getAttributes](reflectionclass.getattributes.html) — Отримує атрибути
-   [ReflectionClass::getConstant](reflectionclass.getconstant.html) — Повертає певну константу
-   [ReflectionClass::getConstants](reflectionclass.getconstants.html) — Повертає константи
-   [ReflectionClass::getConstructor](reflectionclass.getconstructor.html) - Повертає конструктор класу
-   [ReflectionClass::getDefaultProperties](reflectionclass.getdefaultproperties.html) — Повертає властивості за промовчанням
-   [ReflectionClass::getDocComment](reflectionclass.getdoccomment.html) — Повертає doc-блоки коментарів
-   [ReflectionClass::getEndLine](reflectionclass.getendline.html) — Повертає номер останнього рядка
-   [ReflectionClass::getExtension](reflectionclass.getextension.html) — Повертає об'єкт класу ReflectionExtension для модуля, що визначає клас
-   [ReflectionClass::getExtensionName](reflectionclass.getextensionname.html) - Повертає ім'я модуля, що визначає клас
-   [ReflectionClass::getFileName](reflectionclass.getfilename.html) — Повертає ім'я файлу, у якому визначено клас
-   [ReflectionClass::getInterfaceNames](reflectionclass.getinterfacenames.html) — Повертає імена інтерфейсів
-   [ReflectionClass::getInterfaces](reflectionclass.getinterfaces.html) — Повертає інтерфейси
-   [ReflectionClass::getMethod](reflectionclass.getmethod.html) — Повертає екземпляр ReflectionMethod для методу класу
-   [ReflectionClass::getMethods](reflectionclass.getmethods.html) — Повертає список методів у вигляді масиву
-   [ReflectionClass::getModifiers](reflectionclass.getmodifiers.html) — Повертає інформацію про модифікаторів класу
-   [ReflectionClass::getName](reflectionclass.getname.html) - Повертає ім'я класу
-   [ReflectionClass::getNamespaceName](reflectionclass.getnamespacename.html) — Повертає назву простору імен
-   [ReflectionClass::getParentClass](reflectionclass.getparentclass.html) - Повертає батьківський клас
-   [ReflectionClass::getProperties](reflectionclass.getproperties.html) - Повертає властивості
-   [ReflectionClass::getProperty](reflectionclass.getproperty.html) — Повертає екземпляр ReflectionProperty для якості класу
-   [ReflectionClass::getReflectionConstant](reflectionclass.getreflectionconstant.html) — Отримує ReflectionClassConstant для константи класу
-   [ReflectionClass::getReflectionConstants](reflectionclass.getreflectionconstants.html) — Отримує константи класу
-   [ReflectionClass::getShortName](reflectionclass.getshortname.html) - Повертає коротке ім'я
-   [ReflectionClass::getStartLine](reflectionclass.getstartline.html) — Повертає номер початкового рядка
-   [ReflectionClass::getStaticProperties](reflectionclass.getstaticproperties.html) — Повертає статичні властивості
-   [ReflectionClass::getStaticPropertyValue](reflectionclass.getstaticpropertyvalue.html) — Повертає значення статичної властивості
-   [ReflectionClass::getTraitAliases](reflectionclass.gettraitaliases.html) — Повертає масив псевдонімів трейтів
-   [ReflectionClass::getTraitNames](reflectionclass.gettraitnames.html) — Повертає масив імен трейтів, які використовуються у цьому класі
-   [ReflectionClass::getTraits](reflectionclass.gettraits.html) — Повертає масив трейтів, які використовуються у цьому класі.
-   [ReflectionClass::hasConstant](reflectionclass.hasconstant.html) — Перевіряє, чи визначено константу
-   [ReflectionClass::hasMethod](reflectionclass.hasmethod.html) — Перевіряє, чи заданий метод
-   [ReflectionClass::hasProperty](reflectionclass.hasproperty.html) — Перевіряє, чи визначено властивість
-   [ReflectionClass::implementsInterface](reflectionclass.implementsinterface.html) — Перевіряє, чи реалізується інтерфейс
-   [ReflectionClass::inNamespace](reflectionclass.innamespace.html) — Перевіряє, чи визначений клас у просторі імен
-   [ReflectionClass::isAbstract](reflectionclass.isabstract.html) — Перевіряє, чи клас є абстрактним.
-   [ReflectionClass::isAnonymous](reflectionclass.isanonymous.html) — Перевіряє, чи є клас анонімним
-   [ReflectionClass::isCloneable](reflectionclass.iscloneable.html) — Перевіряє, чи можна клонувати цей клас
-   [ReflectionClass::isEnum](reflectionclass.isenum.html) — Повертає, чи є клас перерахуванням
-   [ReflectionClass::isFinal](reflectionclass.isfinal.html) — Перевіряє, чи клас є остаточним (final)
-   [ReflectionClass::isInstance](reflectionclass.isinstance.html) — Перевіряє, чи об'єкт належить класу
-   [ReflectionClass::isInstantiable](reflectionclass.isinstantiable.html) — Перевіряє, чи можна створити екземпляр класу
-   [ReflectionClass::isInterface](reflectionclass.isinterface.html) — Перевіряє, чи клас є інтерфейсом
-   [ReflectionClass::isInternal](reflectionclass.isinternal.html) — Перевіряє, чи є клас вбудованим у модуль чи ядро
-   [ReflectionClass::isIterable](reflectionclass.isiterable.html) — Перевірити, чи клас ітерується.
-   [ReflectionClass::isIterateable](reflectionclass.isiterateable.html) - Псевдонім ReflectionClass::isIterable
-   [ReflectionClass::isSubclassOf](reflectionclass.issubclassof.html) — Перевіряє, чи є клас підкласом
-   [ReflectionClass::isTrait](reflectionclass.istrait.html) — Перевіряє, чи це є трейтом.
-   [ReflectionClass::isUserDefined](reflectionclass.isuserdefined.html) — Перевіряє, чи є клас для користувача
-   [ReflectionClass::newInstance](reflectionclass.newinstance.html) - Створює екземпляр класу з переданими аргументами
-   [ReflectionClass::newInstanceArgs](reflectionclass.newinstanceargs.html) - Створює екземпляр класу з переданими параметрами
-   [ReflectionClass::newInstanceWithoutConstructor](reflectionclass.newinstancewithoutconstructor.html) - Створює новий екземпляр класу без виклику конструктора
-   [ReflectionClass::setStaticPropertyValue](reflectionclass.setstaticpropertyvalue.html) - Встановлює значення статичної властивості
-   [ReflectionClass::\_\_toString](reflectionclass.tostring.html) — Повертає рядкову виставу об'єкта класу ReflectionClass