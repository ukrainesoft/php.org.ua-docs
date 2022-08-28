Клас ComponereMethod

-   [« Componere\\Patch::getClosures](componere-patch.getclosures.html)
    
-   [Componere\\Method::\_\_construct »](componere-method.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Componere](book.componere.html)
    
-   Клас ComponereMethod
    

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

-   [Componere\\Method::\_\_construct](componere-method.construct.html) - Конструктор класу Method
-   [Componere\\Method::setPrivate](componere-method.setprivate.html) — Зміна доступності
-   [Componere\\Method::setProtected](componere-method.setprotected.html) — Зміна доступності
-   [Componere\\Method::setStatic](componere-method.setstatic.html) — Зміна доступності
-   [Componere\\Method::getReflector](componere-method.getreflector.html) - Reflection