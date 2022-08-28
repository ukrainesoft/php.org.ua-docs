Обертає викликаний PHP-об'єкт у LuaSandboxFunction

-   [« LuaSandbox::unpauseUsageTimer](luasandbox.unpauseusagetimer.html)
    
-   [LuaSandboxFunction »](class.luasandboxfunction.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](class.luasandbox.html)
    
-   Обертає викликаний PHP-об'єкт у LuaSandboxFunction
    

# LuaSandbox::wrapPhpFunction

(PECL luasandbox >= 1.2.0)

LuaSandbox::wrapPhpFunction — Обертає викликаний PHP-об'єкт в [LuaSandboxFunction](class.luasandboxfunction.html)

### Опис

```methodsynopsis
public LuaSandbox::wrapPhpFunction(callable $function): LuaSandboxFunction
```

Обертає викликаний PHP-об'єкт в [LuaSandboxFunction](class.luasandboxfunction.html)Тому його можна передати в Lua як анонімну функцію.

Функція повинна повертати або масив значень (який може бути порожнім), або **`null`**що еквівалентно поверненню порожнього масиву.

Винятки виникатимуть як помилки в Lua, проте лише винятки [LuaSandboxRuntimeError](class.luasandboxruntimeerror.html) можуть бути оброблені всередині Lua за допомогою `pcall()` або `xpcall()`

Для отримання додаткової інформації про виклик функцій Lua та значення, що повертаються дивіться [LuaSandboxFunction::call()](luasandboxfunction.call.html)

### Список параметрів

`function`

Функція для обгортання.

### Значення, що повертаються

Повертає [LuaSandboxFunction](class.luasandboxfunction.html)

### Дивіться також

-   [LuaSandbox::loadString()](luasandbox.loadstring.html) - Завантажує код Lua у середу Lua
-   [LuaSandbox::registerLibrary()](luasandbox.registerlibrary.html) - Реєструє набір PHP-функцій як бібліотеку Lua