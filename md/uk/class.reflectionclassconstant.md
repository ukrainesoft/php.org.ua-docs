Клас ReflectionClassConstant

-   [« ReflectionClass::\_\_toString](reflectionclass.tostring.html)
    
-   [ReflectionClassConstant::\_\_construct »](reflectionclassconstant.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionClassConstant
    

# Клас ReflectionClassConstant

(PHP 7> = 7.1.0, PHP 8)

## Вступ

Клас **ReflectionClassConstant** використовується отримання інформації про константах класу.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionClassConstant
     

     implements 
       Reflector {
    /* Константы */
    
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
    
   public __construct(object|string $class, string $constant)

    public static export(mixed $class, string $name, bool $return = ?): string
public getAttributes(?string $name = null, int $flags = 0): array
public getDeclaringClass(): ReflectionClass
public getDocComment(): string|false
public getModifiers(): int
public getName(): string
public getValue(): mixed
public isEnumCase(): bool
public isFinal(): bool
public isPrivate(): bool
public isProtected(): bool
public isPublic(): bool
public __toString(): string

   }
```

## Властивості

name

Ім'я константи класу. Лише читання. У разі спроби зміни викидає виняток [ReflectionException](class.reflectionexception.html)

class

Ім'я класу, у якому визначено константу. Лише читання. У разі спроби зміни викидає виняток [ReflectionException](class.reflectionexception.html)

## Обумовлені константи

## ReflectionClassConstant Modifiers

**`ReflectionClassConstant::IS_PUBLIC`**

Вказує, що константа є [общедоступной](language.oop5.visibility.html). До PHP 7.4.0, значення було `256`

**`ReflectionClassConstant::IS_PROTECTED`**

Вказує, що константа є [защищённой](language.oop5.visibility.html). До PHP 7.4.0, значення було `512`

**`ReflectionClassConstant::IS_PRIVATE`**

Вказує, що константа є [закрытой](language.oop5.visibility.html). До PHP 7.4.0, значення було `1024`

> **Зауваження**
> 
> Ці константи можуть змінюватися від версії до версії PHP. Рекомендується завжди використовувати константи та не покладатися безпосередньо на значення.

## Зміст

-   [ReflectionClassConstant::\_\_construct](reflectionclassconstant.construct.html) — Створює ReflectionClassConstant
-   [ReflectionClassConstant::export](reflectionclassconstant.export.html) - Експорт
-   [ReflectionClassConstant::getAttributes](reflectionclassconstant.getattributes.html) — Отримує атрибути
-   [ReflectionClassConstant::getDeclaringClass](reflectionclassconstant.getdeclaringclass.html) — Отримує оголошуючий клас
-   [ReflectionClassConstant::getDocComment](reflectionclassconstant.getdoccomment.html) — Отримує doc-коментарі
-   [ReflectionClassConstant::getModifiers](reflectionclassconstant.getmodifiers.html) — Отримує модифікатори константи класу
-   [ReflectionClassConstant::getName](reflectionclassconstant.getname.html) — Отримати ім'я константи
-   [ReflectionClassConstant::getValue](reflectionclassconstant.getvalue.html) — Отримує значення
-   [ReflectionClassConstant::isEnumCase](reflectionclassconstant.isenumcase.html) — Перевіряє, чи є константа класу варіантом перерахування
-   [ReflectionClassConstant::isFinal](reflectionclassconstant.isfinal.html) — Перевіряє, чи константа класу є остаточною
-   [ReflectionClassConstant::isPrivate](reflectionclassconstant.isprivate.html) — Перевіряє, чи константа закрита
-   [ReflectionClassConstant::isProtected](reflectionclassconstant.isprotected.html) — Перевіряє, чи константа захищена
-   [ReflectionClassConstant::isPublic](reflectionclassconstant.ispublic.html) — Перевіряє, чи константа є загальнодоступною
-   [ReflectionClassConstant::\_\_toString](reflectionclassconstant.tostring.html) — Повертає строкове представлення об'єкта ReflectionClassConstant