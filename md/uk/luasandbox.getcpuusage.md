Повертає поточний час використання процесора у середовищі Lua

-   [« LuaSandbox::enableProfiler](luasandbox.enableprofiler.html)
    
-   [LuaSandbox::getMemoryUsage »](luasandbox.getmemoryusage.html)
    
-   [PHP Manual](index.html)
    
-   [LuaSandbox](class.luasandbox.html)
    
-   Повертає поточний час використання процесора у середовищі Lua
    

# LuaSandbox::getCPUUsage

(PECL luasandbox >= 1.0.0)

LuaSandbox::getCPUUsage — Повертає поточний час використання процесора в середовищі Lua

### Опис

```methodsynopsis
public LuaSandbox::getCPUUsage(): float
```

Повертає час використання процесора в середовищі Lua.

Включає витрачений час у callback-функціях PHP.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточний час використання процесора за секунди.

> **Зауваження**
> 
> У Windows ця функція завжди повертає нуль. В операційних системах, які не підтримують **`CLOCK_THREAD_CPUTIME_ID`**, таких як FreeBSD і Mac OS X, функція повертає минулий фізичний час, а чи не час процесора.

### Дивіться також

-   [LuaSandbox::getMemoryUsage()](luasandbox.getmemoryusage.html) - Повертає поточне використання пам'яті у середовищі Lua
-   [LuaSandbox::getPeakMemoryUsage()](luasandbox.getpeakmemoryusage.html) - Повертає пікове використання пам'яті в середовищі Lua
-   [LuaSandbox::setCPULimit()](luasandbox.setcpulimit.html) - Встановлює обмеження часу процесора для середовища Lua