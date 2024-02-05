---
navigation:
  - luasandbox.unpauseusagetimer.md: '« LuaSandbox::unpauseUsageTimer'
  - class.luasandboxfunction.md: LuaSandboxFunction »
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::wrapPhpFunction'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::wrapPhpFunction

(PECL luasandbox >= 1.2.0)

LuaSandbox::wrapPhpFunction — Обертає викликаний PHP-об'єкт в [LuaSandboxFunction](class.luasandboxfunction.md)

### Опис

```methodsynopsis
public LuaSandbox::wrapPhpFunction(callable $function): LuaSandboxFunction
```

Обертає викликаний PHP-об'єкт в [LuaSandboxFunction](class.luasandboxfunction.md)Тому його можна передати в Lua як анонімну функцію.

Функція повинна повертати або масив значень (який може бути порожнім), або \*\*`null`\*\*що еквівалентно поверненню порожнього масиву.

Винятки виникатимуть як помилки в Lua, проте лише винятки [LuaSandboxRuntimeError](class.luasandboxruntimeerror.md) можуть бути оброблені всередині Lua за допомогою `pcall()`или`xpcall()`

Для отримання додаткової інформації про виклик функцій Lua та значення, що повертаються дивіться [LuaSandboxFunction::call()](luasandboxfunction.call.md)

### Список параметрів

`function`

Функція для обгортання.

### Значення, що повертаються

Повертає [LuaSandboxFunction](class.luasandboxfunction.md)

### Дивіться також

-   [LuaSandbox::loadString()](luasandbox.loadstring.md) \- Завантажує код Lua у середу Lua
-   [LuaSandbox::registerLibrary()](luasandbox.registerlibrary.md) \- Реєструє набір PHP-функцій як бібліотеку Lua
