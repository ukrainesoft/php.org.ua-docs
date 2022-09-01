---
navigation:
  - luasandbox.wrapphpfunction.md: '« LuaSandbox::wrapPhpFunction'
  - luasandboxfunction.call.md: 'LuaSandboxFunction::call »'
  - index.md: PHP Manual
  - book.luasandbox.md: LuaSandbox
title: Клас LuaSandboxFunction
---
# Клас LuaSandboxFunction

(PECL luasandbox >= 1.0.0)

## Вступ

Представляє функцію Lua, що дозволяє викликати її з PHP.

Функція LuaSandboxFunction може бути отримана як значення, що повертається з Lua, як параметр, переданий в callback-функцію з Lua, або за допомогою [LuaSandbox::wrapPhpFunction()](luasandbox.wrapphpfunction.md) [LuaSandbox::loadString()](luasandbox.loadstring.md) або [LuaSandbox::loadBinary()](luasandbox.loadbinary.md)

## Огляд класів

```classsynopsis



    
     
      class LuaSandboxFunction
     
     {


    /* Методы */
    
   public call(string ...$args): array|bool
public dump(): string

   }
```

## Зміст

-   [LuaSandboxFunction::call](luasandboxfunction.call.md) - Викликає Lua-функцію
-   [LuaSandboxFunction::construct](luasandboxfunction.construct.md) - Не використовується
-   [LuaSandboxFunction::dump](luasandboxfunction.dump.md) — Вивантажує функцію у вигляді BLOB
