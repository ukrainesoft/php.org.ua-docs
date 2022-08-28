Клас ReflectionReference

-   [« ReflectionIntersectionType::getTypes](reflectionintersectiontype.gettypes.html)
    
-   [ReflectionReference::\_\_construct »](reflectionreference.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Reflection](book.reflection.html)
    
-   Клас ReflectionReference
    

# Клас ReflectionReference

(PHP 7> = 7.4.0, PHP 8)

## Вступ

Клас **ReflectionReference** надає інформацію про посилання.

## Огляд класів

```classsynopsis

     
    

    
     
      final
      class ReflectionReference
     
     {

    /* Методы */
    
   private __construct()

    public static fromArrayElement(array $array, int|string $key): ?ReflectionReference
public getId(): string

   }
```

## Зміст

-   [ReflectionReference::\_\_construct](reflectionreference.construct.html) — Закритий конструктор, який забороняє створення екземпляра безпосередньо
-   [ReflectionReference::fromArrayElement](reflectionreference.fromarrayelement.html) — Створює ReflectionReference із елементу масиву
-   [ReflectionReference::getId](reflectionreference.getid.html) — Отримати унікальний ідентифікатор посилання