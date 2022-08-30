Клас ComponereMethod

-   [« ComponerePatch::getClosures](componere-patch.getclosures.html)
    
-   [ComponereMethod::construct »](componere-method.construct.html)
    
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

-   [ComponereMethod::construct](componere-method.construct.html) - Конструктор класу Method
-   [ComponereMethod::setPrivate](componere-method.setprivate.html) — Зміна доступності
-   [ComponereMethod::setProtected](componere-method.setprotected.html) — Зміна доступності
-   [ComponereMethod::setStatic](componere-method.setstatic.html) — Зміна доступності
-   [ComponereMethod::getReflector](componere-method.getreflector.html) - Reflection