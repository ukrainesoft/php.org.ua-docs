---
navigation:
  - lua.registercallback.md: '« Lua::registerCallback'
  - luaclosure.invoke.md: 'LuaClosure::\_\_invoke »'
  - index.md: PHP Manual
  - book.lua.md: Lua
title: Клас LuaClosure
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас LuaClosure

(PECL lua >=0.9.0)

## Вступ

LuaClosure - це клас обгортка для LUA\_TFUNCTION, яка може бути повернена під час виклику функції Lua.

## Огляд класів

```classsynopsis


    
    
     
      class LuaClosure
     
     {
    

    /* Методы */
    
   public __invoke(mixed ...$args): void

   }
```

## Зміст

-   [LuaClosure::\_\_invoke](luaclosure.invoke.md)— Виклик замикання Lua
