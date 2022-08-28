Клас ComponereValue

-   [« Componere\\Method::getReflector](componere-method.getreflector.html)
    
-   [Componere\\Value::\_\_construct »](componere-value.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Componere](book.componere.html)
    
-   Клас ComponereValue
    

# Клас ComponereValue

(Componere 2 >= 2.1.0)

## Вступ

Value являє собою змінну PHP всіх типів, включаючи невизначену (undefined)

## Огляд класів

```classsynopsis



    
     
      final
      class Componere\Value
     
     {


    /* Конструктор класса */
    
   public __construct( $default = ?)


    /* Методы */
    public setPrivate(): Value
public setProtected(): Value
public setStatic(): Value
public isPrivate(): bool
public isProtected(): bool
public isStatic(): bool
public hasDefault(): bool

   }
```

## Зміст

-   [Componere\\Value::\_\_construct](componere-value.construct.html) - Конструктор класу Value
-   [Componere\\Value::setPrivate](componere-value.setprivate.html) — Зміна доступності
-   [Componere\\Value::setProtected](componere-value.setprotected.html) — Зміна доступності
-   [Componere\\Value::setStatic](componere-value.setstatic.html) — Зміна доступності
-   [Componere\\Value::isPrivate](componere-value.isprivate.html) — Визначення доступності
-   [Componere\\Value::isProtected](componere-value.isprotected.html) — Визначення доступності
-   [Componere\\Value::isStatic](componere-value.isstatic.html) — Визначення доступності
-   [Componere\\Value::hasDefault](componere-value.hasdefault.html) - Взаємодія з класом Value