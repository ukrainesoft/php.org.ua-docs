---
navigation:
  - componere-patch.getclosures.md: '« Componere\\Patch::getClosures'
  - componere-method.construct.md: 'Componere\\Method::\_\_construct »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас Componere\\Method
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Componere\\Method

(Componere 2 >= 2.1.0)

## Вступ

Method представляє функцію зі змінними прапорами доступності

## Огляд класів

```classsynopsis



    
     
      final
      class Componere\Method
     
     {


    /* Конструктор класса */
    
   public __construct(Closure $closure)


    /* Методы */
    public setPrivate(): Method
public setProtected(): Method
public setStatic(): Method
public getReflector(): ReflectionMethod

   }
```

## Зміст

-   [Componere\\Method::\_\_construct](componere-method.construct.md) \- Конструктор класу Method
-   [Componere\\Method::setPrivate](componere-method.setprivate.md)— Зміна доступності
-   [Componere\\Method::setProtected](componere-method.setprotected.md)— Зміна доступності
-   [Componere\\Method::setStatic](componere-method.setstatic.md)— Зміна доступності
-   [Componere\\Method::getReflector](componere-method.getreflector.md)— Reflection
