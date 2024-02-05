---
navigation:
  - luasandbox.disableprofiler.md: '« LuaSandbox::disableProfiler'
  - luasandbox.getcpuusage.md: 'LuaSandbox::getCPUUsage »'
  - index.md: PHP Manual
  - class.luasandbox.md: LuaSandbox
title: 'LuaSandbox::enableProfiler'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# LuaSandbox::enableProfiler

(PECL luasandbox >= 1.1.0)

LuaSandbox::enableProfiler — Включає профільувальник

### Опис

```methodsynopsis
public LuaSandbox::enableProfiler(float $period = 0.02): bool
```

Вмикає профільувальник. Профілювання розпочнеться після введення коду Lua.

Профілювальник періодично проводить вимірювання середовища Lua для запису виконуваної функції. Тестування показує, що принаймні в Linux установка періоду менше 1 мілісекунд призведе до великої кількості переповнень, але без проблем з продуктивністю.

### Список параметрів

`period`

Період вибірки за секунди.

### Значення, що повертаються

Повертає логічне значення, що вказує на те, чи включений профільник.

### Дивіться також

-   [LuaSandbox::disableProfiler()](luasandbox.disableprofiler.md) \- відключає профільник
-   [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.md) \- Отримує дані профілювача
