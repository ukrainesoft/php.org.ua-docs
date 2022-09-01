---
navigation:
  - componere-method.getreflector.html: '« ComponereMethod::getReflector'
  - componere-value.construct.html: 'ComponereValue::construct »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас ComponereValue
---
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

-   [ComponereValue::construct](componere-value.construct.html) - Конструктор класу Value
-   [ComponereValue::setPrivate](componere-value.setprivate.html) — Зміна доступності
-   [ComponereValue::setProtected](componere-value.setprotected.html) — Зміна доступності
-   [ComponereValue::setStatic](componere-value.setstatic.html) — Зміна доступності
-   [ComponereValue::isPrivate](componere-value.isprivate.html) — Визначення доступності
-   [ComponereValue::isProtected](componere-value.isprotected.html) — Визначення доступності
-   [ComponereValue::isStatic](componere-value.isstatic.html) — Визначення доступності
-   [ComponereValue::hasDefault](componere-value.hasdefault.html) - Взаємодія з класом Value
