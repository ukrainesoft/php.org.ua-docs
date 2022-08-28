Клас ReflectionZendExtension

-   [« ReflectionEnumBackedCase::getBackingValue](reflectionenumbackedcase.getbackingvalue.html)
    
-   [ReflectionZendExtension::\_\_clone »](reflectionzendextension.clone.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionZendExtension
    

# Клас ReflectionZendExtension

(PHP 5> = 5.4.0, PHP 7, PHP 8)

## Вступ

## Огляд класів

```classsynopsis

     
    

    
     
      class ReflectionZendExtension
     

     implements 
       Reflector {

    /* Свойства */
    
     public
     string
      $name;


    /* Методы */
    
   public __construct(string $name)

    private __clone(): void
public static export(string $name, bool $return = ?): string
public getAuthor(): string
public getCopyright(): string
public getName(): string
public getURL(): string
public getVersion(): string
public __toString(): string

   }
```

## Властивості

name

Ім'я модуль. Доступно тільки для читання та викидає виняток [ReflectionException](class.reflectionexception.html) під час спроби запису.

## Зміст

-   [ReflectionZendExtension::\_\_clone](reflectionzendextension.clone.html) - Обробник клонування
-   [ReflectionZendExtension::\_\_construct](reflectionzendextension.construct.html) - Конструктор
-   [ReflectionZendExtension::export](reflectionzendextension.export.html) - Експорт
-   [ReflectionZendExtension::getAuthor](reflectionzendextension.getauthor.html) — Отримує автора
-   [ReflectionZendExtension::getCopyright](reflectionzendextension.getcopyright.html) — Отримує авторські права
-   [ReflectionZendExtension::getName](reflectionzendextension.getname.html) — Отримує ім'я
-   [ReflectionZendExtension::getURL](reflectionzendextension.geturl.html) — Отримує URL
-   [ReflectionZendExtension::getVersion](reflectionzendextension.getversion.html) — Отримує версію
-   [ReflectionZendExtension::\_\_toString](reflectionzendextension.tostring.html) - Обробник перетворення в рядок