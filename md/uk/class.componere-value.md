---
navigation:
  - componere-method.getreflector.md: '« Componere\\Method::getReflector'
  - componere-value.construct.md: 'Componere\\Value::\_\_construct »'
  - index.md: PHP Manual
  - book.componere.md: Componere
title: Клас Componere\\Value
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Componere\\Value

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

-   [Componere\\Value::\_\_construct](componere-value.construct.md) \- Конструктор класу Value
-   [Componere\\Value::setPrivate](componere-value.setprivate.md)— Зміна доступності
-   [Componere\\Value::setProtected](componere-value.setprotected.md)— Зміна доступності
-   [Componere\\Value::setStatic](componere-value.setstatic.md)— Зміна доступності
-   [Componere\\Value::isPrivate](componere-value.isprivate.md)— Визначення доступності
-   [Componere\\Value::isProtected](componere-value.isprotected.md)— Визначення доступності
-   [Componere\\Value::isStatic](componere-value.isstatic.md)— Визначення доступності
-   [Componere\\Value::hasDefault](componere-value.hasdefault.md) \- Взаємодія з класом Value
