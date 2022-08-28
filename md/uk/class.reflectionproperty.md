Клас ReflectionProperty

-   [« ReflectionParameter::\_\_toString](reflectionparameter.tostring.html)
    
-   [ReflectionProperty::\_\_clone »](reflectionproperty.clone.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionProperty
    

# Клас ReflectionProperty

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **ReflectionProperty** повідомляє інформацію про властивості класу.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionProperty
     

     implements 
       Reflector {
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
public setValue(mixed $value): void
public __toString(): string

   }
```

## Властивості

name

Ім'я якості. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.html) під час спроби запису.

class

Ім'я класу, в якому цю властивість описано. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.html) під час спроби запису.

## Обумовлені константи

## Модифікатори ReflectionProperty

**`ReflectionProperty::IS_STATIC`**

Вказує, що властивість є [статическим](language.oop5.static.html). До PHP 7.4.0, значення було `1`

**`ReflectionProperty::IS_PUBLIC`**

Вказує, що властивість є [общедоступным](language.oop5.visibility.html). До PHP 7.4.0, значення було `256`

**`ReflectionProperty::IS_PROTECTED`**

Вказує, що властивість є [защищённым](language.oop5.visibility.html). До PHP 7.4.0, значення було `512`

**`ReflectionProperty::IS_PRIVATE`**

Вказує, що властивість є [закрытым](language.oop5.visibility.html). До PHP 7.4.0, значення було `1024`

> **Зауваження**
> 
> Ці константи можуть змінюватися від версії до версії PHP. Рекомендується завжди використовувати константи та не покладатися безпосередньо на значення.

## Зміст

-   [ReflectionProperty::\_\_clone](reflectionproperty.clone.html) - Клонувати
-   [ReflectionProperty::\_\_construct](reflectionproperty.construct.html) - Конструктор класу ReflectionProperty
-   [ReflectionProperty::export](reflectionproperty.export.html) - Експорт
-   [ReflectionProperty::getAttributes](reflectionproperty.getattributes.html) — Отримує атрибути
-   [ReflectionProperty::getDeclaringClass](reflectionproperty.getdeclaringclass.html) — Отримання класу, що оголошує
-   [ReflectionProperty::getDefaultValue](reflectionproperty.getdefaultvalue.html) — Повертає значення за промовчанням, задане для якості
-   [ReflectionProperty::getDocComment](reflectionproperty.getdoccomment.html) — Отримання doc-коментаря для якості
-   [ReflectionProperty::getModifiers](reflectionproperty.getmodifiers.html) - Отримання модифікаторів властивостей класу
-   [ReflectionProperty::getName](reflectionproperty.getname.html) - Отримання імені властивості
-   [ReflectionProperty::getType](reflectionproperty.gettype.html) — Отримати тип якості
-   [ReflectionProperty::getValue](reflectionproperty.getvalue.html) — Отримує значення
-   [ReflectionProperty::hasDefaultValue](reflectionproperty.hasdefaultvalue.html) — Перевіряє, чи встановлено значення за промовчанням для властивості.
-   [ReflectionProperty::hasType](reflectionproperty.hastype.html) — Перевірити, чи заданий для якості тип
-   [ReflectionProperty::isDefault](reflectionproperty.isdefault.html) — Перевіряє, чи значення є властивістю за умовчанням
-   [ReflectionProperty::isInitialized](reflectionproperty.isinitialized.html) — Перевірити, чи ініціалізована властивість
-   [ReflectionProperty::isPrivate](reflectionproperty.isprivate.html) — Перевіряє, чи властивість закрита.
-   [ReflectionProperty::isPromoted](reflectionproperty.ispromoted.html) — Перевіряє, чи визначено властивість у конструкторі
-   [ReflectionProperty::isProtected](reflectionproperty.isprotected.html) — Перевіряє, чи властивість захищена
-   [ReflectionProperty::isPublic](reflectionproperty.ispublic.html) — Перевіряє, чи є властивість загальнодоступною.
-   [ReflectionProperty::isReadOnly](reflectionproperty.isreadonly.html) — Перевіряє, чи властивість є readonly-властивістю
-   [ReflectionProperty::isStatic](reflectionproperty.isstatic.html) — Перевірка, чи властивість статична
-   [ReflectionProperty::setAccessible](reflectionproperty.setaccessible.html) — Робить властивість доступною
-   [ReflectionProperty::setValue](reflectionproperty.setvalue.html) - Встановлення значення властивості
-   [ReflectionProperty::\_\_toString](reflectionproperty.tostring.html) — Перетворення на рядок