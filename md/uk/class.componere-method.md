---
navigation:
  - componere-patch.getclosures.md: '« ComponerePatch::getClosures'
  - componere-method.construct.md: 'ComponereMethod::construct »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас ComponereMethod
---
# Клас ComponereMethod

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

-   [ComponereMethod::construct](componere-method.construct.md) - Конструктор класу Method
-   [ComponereMethod::setPrivate](componere-method.setprivate.md) — Зміна доступності
-   [ComponereMethod::setProtected](componere-method.setprotected.md) — Зміна доступності
-   [ComponereMethod::setStatic](componere-method.setstatic.md) — Зміна доступності
-   [ComponereMethod::getReflector](componere-method.getreflector.md) - Reflection
