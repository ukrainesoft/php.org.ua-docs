---
navigation:
  - luasandbox.disableprofiler.html: '« LuaSandbox::disableProfiler'
  - luasandbox.getcpuusage.html: 'LuaSandbox::getCPUUsage »'
  - index.html: PHP Manual
  - class.luasandbox.html: LuaSandbox
title: 'LuaSandbox::enableProfiler'
---
# LuaSandbox::enableProfiler

(PECL luasandbox >= 1.1.0)

LuaSandbox::enableProfiler — Включає профільувальник

### Опис

```methodsynopsis
public LuaSandbox::enableProfiler(float $period = 0.02): bool
```

Вмикає профільувальник. Профілювання розпочнеться після введення коду Lua.

Профілювальник періодично проводить вимірювання середовища Lua для запису функції, що виконується. Тестування показує, що принаймні в Linux установка періоду менше 1 мілісекунд призведе до великої кількості переповнень, але без проблем з продуктивністю.

### Список параметрів

`period`

Період вибірки за секунди.

### Значення, що повертаються

Повертає логічне значення, що вказує на те, чи включений профільник.

### Дивіться також

-   [LuaSandbox::disableProfiler()](luasandbox.disableprofiler.html) - відключає профільник
-   [LuaSandbox::getProfilerFunctionReport()](luasandbox.getprofilerfunctionreport.html) - Отримує дані профілювача
