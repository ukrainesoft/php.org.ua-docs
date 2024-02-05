---
navigation:
  - reflectionparameter.tostring.md: '« ReflectionParameter::\_\_function toString() { [native code] }'
  - reflectionproperty.clone.md: 'ReflectionProperty::\_\_clone »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionProperty
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас ReflectionProperty

(PHP 5, PHP 7, PHP 8)

## Вступ

Класс**ReflectionProperty** повідомляє інформацію про властивості класу.

## Огляд класів

```classsynopsis

    
     class ReflectionProperty
    

    
     implements
      Reflector {

    /* Константы */
    
     public
     const
     int
      IS_STATIC;

    public
     const
     int
      IS_READONLY;

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


    /* Свойства */
    public
     string
      $name;

    public
     string
      $class;


    /* Методы */
    
   public __construct(object|string $class, string $property)

    private __clone(): void
public static export(mixed $class, string $name, bool $return = ?): string
public getAttributes(?string $name = null, int $flags = 0): array
public getDeclaringClass(): ReflectionClass
public getDefaultValue(): mixed
public getDocComment(): string|false
public getModifiers(): int
public getName(): string
public getType(): ?ReflectionType
public getValue(?object $object = null): mixed
public hasDefaultValue(): bool
public hasType(): bool
public isDefault(): bool
public isInitialized(?object $object = null): bool
public isPrivate(): bool
public isPromoted(): bool
public isProtected(): bool
public isPublic(): bool
public isReadOnly(): bool
public isStatic(): bool
public setAccessible(bool $accessible): void
public setValue(object $object, mixed $value): void
public __toString(): string

   }
```

## Властивості

name

Ім'я якості. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.md) під час спроби запису.

class

Ім'я класу, в якому цю властивість описано. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.md) під час спроби запису.

## Обумовлені константи

## Модифікатори ReflectionProperty

**`ReflectionProperty::IS_STATIC`**

Вказує, що властивість є [статичним](language.oop5.static.md). До PHP 7.4.0, значення було

**`ReflectionProperty::IS_READONLY`**

Вказує, що властивість є [доступним лише для читання](language.oop5.properties.md#language.oop5.properties.readonly-properties). Доступно з PHP 8.1.0.

**`ReflectionProperty::IS_PUBLIC`**

Вказує, що властивість є [загальнодоступним](language.oop5.visibility.md). До PHP 7.4.0, значення було `256`

**`ReflectionProperty::IS_PROTECTED`**

Вказує, що властивість є [захищеним](language.oop5.visibility.md). До PHP 7.4.0, значення було `512`

**`ReflectionProperty::IS_PRIVATE`**

Вказує, що властивість є [закритим](language.oop5.visibility.md). До PHP 7.4.0, значення було `1024`

> **Зауваження** :
> 
> Ці константи можуть змінюватися від версії до версії PHP. Рекомендується завжди використовувати константи і не покладатися безпосередньо на значення.

## список змін

| Версия | Опис |
| --- | --- |
| 8.0.0 | Метод[ReflectionProperty::export()](reflectionproperty.export.md)був видалений. |

## Зміст

-   [ReflectionProperty::\_\_clone](reflectionproperty.clone.md) \- Клонувати
-   [ReflectionProperty::\_\_construct](reflectionproperty.construct.md) \- Конструктор класу ReflectionProperty
-   [ReflectionProperty::export](reflectionproperty.export.md) \- Експорт
-   [ReflectionProperty::getAttributes](reflectionproperty.getattributes.md)— Отримує атрибути
-   [ReflectionProperty::getDeclaringClass](reflectionproperty.getdeclaringclass.md)— Отримання класу, що оголошує
-   [ReflectionProperty::getDefaultValue](reflectionproperty.getdefaultvalue.md)— Повертає значення за промовчанням, задане для якості
-   [ReflectionProperty::getDocComment](reflectionproperty.getdoccomment.md)— Отримання doc-коментаря для якості
-   [ReflectionProperty::getModifiers](reflectionproperty.getmodifiers.md) \- Отримання модифікаторів властивостей класу
-   [ReflectionProperty::getName](reflectionproperty.getname.md) \- Отримання імені властивості
-   [ReflectionProperty::getType](reflectionproperty.gettype.md)— Отримати тип якості
-   [ReflectionProperty::getValue](reflectionproperty.getvalue.md)— Отримує значення
-   [ReflectionProperty::hasDefaultValue](reflectionproperty.hasdefaultvalue.md)— Перевіряє, чи встановлено значення за промовчанням для властивості.
-   [ReflectionProperty::hasType](reflectionproperty.hastype.md)— Перевірити, чи заданий для якості тип
-   [ReflectionProperty::isDefault](reflectionproperty.isdefault.md)— Перевіряє, чи значення є властивістю за умовчанням
-   [ReflectionProperty::isInitialized](reflectionproperty.isinitialized.md)— Перевірити, чи ініціалізована властивість
-   [ReflectionProperty::isPrivate](reflectionproperty.isprivate.md)— Перевіряє, чи властивість закрита.
-   [ReflectionProperty::isPromoted](reflectionproperty.ispromoted.md)— Перевіряє, чи визначено властивість у конструкторі
-   [ReflectionProperty::isProtected](reflectionproperty.isprotected.md)— Перевіряє, чи властивість захищена
-   [ReflectionProperty::isPublic](reflectionproperty.ispublic.md)— Перевіряє, чи є властивість загальнодоступною.
-   [ReflectionProperty::isReadOnly](reflectionproperty.isreadonly.md)— Перевіряє, чи властивість є readonly-властивістю
-   [ReflectionProperty::isStatic](reflectionproperty.isstatic.md)— Перевірка, чи властивість статична
-   [ReflectionProperty::setAccessible](reflectionproperty.setaccessible.md)— Робить властивість доступною
-   [ReflectionProperty::setValue](reflectionproperty.setvalue.md) \- Встановлення значення властивості
-   [ReflectionProperty::\_\_function toString() { \[native code\] }](reflectionproperty.tostring.md)— Перетворення на рядок
