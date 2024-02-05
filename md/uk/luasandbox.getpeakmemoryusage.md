---
navigation:
  - luasandbox.getmemoryusage.md: '« LuaSandbox::getMemoryUsage'
  - luasandbox.getprofilerfunctionreport.md: 'LuaSandbox::getProfilerFunctionReport »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::getPeakMemoryUsage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::getPeakMemoryUsage

(PECL luasandbox >= 1.0.0)

LuaSandbox::getPeakMemoryUsage — Повертає пікове використання пам'яті в середовищі Lua

### Опис

```methodsynopsis
public LuaSandbox::getPeakMemoryUsage(): int
```

Повертає пікове використання пам'яті у середовищі Lua.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає пікове використання пам'яті в байтах.

### Дивіться також

-   [LuaSandbox::getMemoryUsage()](luasandbox.getmemoryusage.md) \- Повертає поточне використання пам'яті у середовищі Lua
-   [LuaSandbox::getCPUUsage()](luasandbox.getcpuusage.md) \- Повертає поточний час використання процесора у середовищі Lua
-   [LuaSandbox::setMemoryLimit()](luasandbox.setmemorylimit.md) \- Встановлює межу пам'яті для середовища Lua
