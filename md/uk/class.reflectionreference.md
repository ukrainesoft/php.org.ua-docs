---
navigation:
  - reflectionintersectiontype.gettypes.md: '« ReflectionIntersectionType::getTypes'
  - reflectionreference.construct.md: 'ReflectionReference::construct »'
  - index.md: PHP Manual
  - book.reflection.md: Reflection
title: Клас ReflectionReference
---
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

-   [ReflectionReference::construct](reflectionreference.construct.md) — Закритий конструктор, який забороняє створення екземпляра безпосередньо
-   [ReflectionReference::fromArrayElement](reflectionreference.fromarrayelement.md) — Створює ReflectionReference із елементу масиву
-   [ReflectionReference::getId](reflectionreference.getid.md) — Отримати унікальний ідентифікатор посилання
