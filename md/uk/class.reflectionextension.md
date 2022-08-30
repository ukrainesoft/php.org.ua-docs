Клас ReflectionExtension

-   [« ReflectionZendExtension::toString](reflectionzendextension.tostring.html)
    
-   [ReflectionExtension::clone »](reflectionextension.clone.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionExtension
    

# Клас ReflectionExtension

(PHP 5, PHP 7, PHP 8)

## Вступ

Клас **ReflectionExtension** повідомляє інформацію про модулі.

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionExtension
     

     implements 
       Reflector {

    /* Свойства */
    
     public
     string
      $name;


    /* Методы */
    
   public __construct(string $name)

    private __clone(): void
public static export(string $name, string $return = false): string
public getClasses(): array
public getClassNames(): array
public getConstants(): array
public getDependencies(): array
public getFunctions(): array
public getINIEntries(): array
public getName(): string
public getVersion(): ?string
public info(): void
public isPersistent(): bool
public isTemporary(): bool
public __toString(): string

   }
```

## Властивості

name

Ім'я модуль. Значення властивості збігається з тим, що метод повертає метод [ReflectionExtension::getName()](reflectionextension.getname.html)

## Зміст

-   [ReflectionExtension::clone](reflectionextension.clone.html) - Клонує об'єкт
-   [ReflectionExtension::construct](reflectionextension.construct.html) — Створює об'єкт класу ReflectionExtension
-   [ReflectionExtension::export](reflectionextension.export.html) - Експортує модуль
-   [ReflectionExtension::getClasses](reflectionextension.getclasses.html) - Повертає класи
-   [ReflectionExtension::getClassNames](reflectionextension.getclassnames.html) - Отримання імен класів
-   [ReflectionExtension::getConstants](reflectionextension.getconstants.html) - Отримання констант
-   [ReflectionExtension::getDependencies](reflectionextension.getdependencies.html) - Отримання залежностей
-   [ReflectionExtension::getFunctions](reflectionextension.getfunctions.html) — Отримання функцій модуля
-   [ReflectionExtension::getINIEntries](reflectionextension.getinientries.html) — Отримання ini-налаштувань модуля
-   [ReflectionExtension::getName](reflectionextension.getname.html) — Отримання імені модуля
-   [ReflectionExtension::getVersion](reflectionextension.getversion.html) — Отримання версії модуля
-   [ReflectionExtension::info](reflectionextension.info.html) — Виведення інформації про модуль
-   [ReflectionExtension::isPersistent](reflectionextension.ispersistent.html) — Визначає, чи модуль є постійним
-   [ReflectionExtension::isTemporary](reflectionextension.istemporary.html) — Визначає, чи модуль є тимчасовим
-   [ReflectionExtension::toString](reflectionextension.tostring.html) — Перетворення на рядок