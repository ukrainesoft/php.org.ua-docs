Клас LuaClosure

-   [« Lua::registerCallback](lua.registercallback.md)
    
-   [LuaClosure::invoke »](luaclosure.invoke.md)
    
-   [PHP Manual](index.md)
    
-   [Lua](book.lua.md)
    
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

-   [LuaClosure::invoke](luaclosure.invoke.md) — Виклик замикання Lua