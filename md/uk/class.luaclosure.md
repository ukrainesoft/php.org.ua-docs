---
navigation:
  - lua.registercallback.md: '« Lua::registerCallback'
  - luaclosure.invoke.md: 'LuaClosure::invoke »'
  - index.md: PHP Manual
  - book.lua.md: Lua
title: Клас LuaClosure
---
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
