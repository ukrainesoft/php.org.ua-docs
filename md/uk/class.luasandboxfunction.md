Клас LuaSandboxFunction

-   [« LuaSandbox::wrapPhpFunction](luasandbox.wrapphpfunction.html)
    
-   [LuaSandboxFunction::call »](luasandboxfunction.call.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](book.luasandbox.html)
    
-   Клас LuaSandboxFunction
    

# Клас LuaSandboxFunction

(PECL luasandbox >= 1.0.0)

## Вступ

Представляє функцію Lua, що дозволяє викликати її з PHP.

Функція LuaSandboxFunction може бути отримана як значення, що повертається з Lua, як параметр, переданий в callback-функцію з Lua, або за допомогою [LuaSandbox::wrapPhpFunction()](luasandbox.wrapphpfunction.html) [LuaSandbox::loadString()](luasandbox.loadstring.html) або [LuaSandbox::loadBinary()](luasandbox.loadbinary.html)

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

-   [LuaSandboxFunction::call](luasandboxfunction.call.html) - Викликає Lua-функцію
-   [LuaSandboxFunction::\_\_construct](luasandboxfunction.construct.html) - Не використовується
-   [LuaSandboxFunction::dump](luasandboxfunction.dump.html) — Вивантажує функцію у вигляді BLOB