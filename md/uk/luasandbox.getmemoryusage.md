---
navigation:
  - luasandbox.getcpuusage.md: '« LuaSandbox::getCPUUsage'
  - luasandbox.getpeakmemoryusage.md: 'LuaSandbox::getPeakMemoryUsage »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::getMemoryUsage'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::getMemoryUsage

(PECL luasandbox >= 1.0.0)

LuaSandbox::getMemoryUsage — Повертає поточне використання пам'яті в середовищі Lua

### Опис

```methodsynopsis
public LuaSandbox::getMemoryUsage(): int
```

Повертає поточне використання пам'яті серед Lua.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає поточне використання пам'яті у байтах.

### Дивіться також

-   [LuaSandbox::getPeakMemoryUsage()](luasandbox.getpeakmemoryusage.md) \- Повертає пікове використання пам'яті в середовищі Lua
-   [LuaSandbox::getCPUUsage()](luasandbox.getcpuusage.md) \- Повертає поточний час використання процесора у середовищі Lua
-   [LuaSandbox::setMemoryLimit()](luasandbox.setmemorylimit.md) \- Встановлює межу пам'яті для середовища Lua
