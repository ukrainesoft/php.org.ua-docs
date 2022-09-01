---
navigation:
  - lua.resources.html: « Типи ресурсів
  - lua.assign.html: 'Lua::assign »'
  - index.html: PHP Manual
  - book.lua.html: Lua
title: Клас Lua
---
# Клас Lua

(PECL lua> = 0.9.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class Lua
     
     {
    
    /* Константы */
    
     const
     string
      LUA_VERSION = Lua 5.1.4;


    /* Методы */
    
   public assign(string $name, string $value): mixed
public call(callable $lua_func, array $args = ?, int $use_self = 0): mixed
public __call(callable $lua_func, array $args = ?, int $use_self = 0): mixed
public __construct(string $lua_script_file = NULL)
public eval(string $statements): mixed
public getVersion(): string
public include(string $file): mixed
public registerCallback(string $name, callable $function): mixed

   }
```

## Обумовлені константи

**`Lua::LUA_VERSION`**

## Зміст

-   [Lua::assign](lua.assign.html) - Присвоїти PHP-змінної Lua
-   [Lua::call](lua.call.html) — Викликати функції Lua
-   [Lua::construct](lua.construct.html) - Конструктор Lua
-   [Lua::eval](lua.eval.html) - Розбирає рядок як код Lua
-   [Lua::getVersion](lua.getversion.html) — Повертає версію
-   [Lua::include](lua.include.html) — Розбирає файл, що містить скрипт Lua
-   [Lua::registerCallback](lua.registercallback.html) — Зареєструвати функцію PHP у Lua
