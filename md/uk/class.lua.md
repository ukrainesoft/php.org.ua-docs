---
navigation:
  - lua.resources.md: « Типи ресурсів
  - lua.assign.md: 'Lua::assign »'
  - index.md: PHP Manual
  - book.lua.md: Lua
title: Клас Lua
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Lua

(PECL lua >=0.9.0)

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

-   [Lua::assign](lua.assign.md) \- Присвоїти PHP-змінної Lua
-   [Lua::call](lua.call.md)— Викликати функції Lua
-   [Lua::\_\_construct](lua.construct.md) \- Конструктор Lua
-   [Lua::eval](lua.eval.md) \- Розбирає рядок як код Lua
-   [Lua::getVersion](lua.getversion.md)— Повертає версію
-   [Lua::include](lua.include.md)— Розбирає файл, що містить скрипт Lua
-   [Lua::registerCallback](lua.registercallback.md)— Зареєструвати функцію PHP у Lua
