---
navigation:
  - luasandbox.enableprofiler.md: '« LuaSandbox::enableProfiler'
  - luasandbox.getmemoryusage.md: 'LuaSandbox::getMemoryUsage »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::getCPUUsage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

Повертає час використання процесора в секундах.

> **Зауваження** :
> 
> У Windows ця функція завжди повертає нуль. В операційних системах, які не підтримують **`CLOCK_THREAD_CPUTIME_ID`**, таких як FreeBSD і Mac OS X, функція повертає минулий фізичний час, а чи не час процесора.

### Дивіться також

-   [LuaSandbox::getMemoryUsage()](luasandbox.getmemoryusage.md) \- Повертає поточне використання пам'яті у середовищі Lua
-   [LuaSandbox::getPeakMemoryUsage()](luasandbox.getpeakmemoryusage.md) \- Повертає пікове використання пам'яті в середовищі Lua
-   [LuaSandbox::setCPULimit()](luasandbox.setcpulimit.md) \- Встановлює обмеження часу процесора для середовища Lua
