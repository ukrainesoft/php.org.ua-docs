Клас LuaClosure

-   [« Lua::registerCallback](lua.registercallback.html)
    
-   [LuaClosure::invoke »](luaclosure.invoke.html)
    
-   [PHP Manual](index.html)
    
-   [Lua](book.lua.html)
    
-   Клас LuaClosure
    

# Клас LuaClosure

(PECL lua> = 0.9.0)

## Вступ

Lua Closure – це клас обгортка для LUATFUNCTION, яка може бути повернена під час виклику функції Lua.

## Огляд класів

```classsynopsis


    
    
     
      class LuaClosure
     
     {
    

    /* Методы */
    
   public __invoke(mixed ...$args): void

   }
```

## Зміст

-   [LuaClosure::invoke](luaclosure.invoke.html) — Виклик замикання Lua