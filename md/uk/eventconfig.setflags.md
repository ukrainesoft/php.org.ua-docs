---
navigation:
  - eventconfig.requirefeatures.md: '« EventConfig::requireFeatures'
  - eventconfig.setmaxdispatchinterval.md: 'EventConfig::setMaxDispatchInterval »'
  - index.md: PHP Manual
  - class.eventconfig.md: EventConfig
title: 'EventConfig::setFlags'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventConfig::setFlags

(PECL event >= 2.0.2-alpha)

EventConfig::setFlags — Встановлює один або кілька прапорів для налаштування можливої ​​ініціалізації EventBase

### Опис

```methodsynopsis
public
   EventConfig::setFlags(
    int
     $flags
   ): bool
```

Встановлює один або кілька прапорів для налаштування того, які частини можливої ​​EventBase будуть ініціалізовані та як вони працюватимуть.

### Список параметрів

`flags`

Одна из констант`EventBase::LOOP_*`Смотрите[константи EventBase](class.eventbase.md#eventbase.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBase::getFeatures()](eventbase.getfeatures.md) \- Повертає бітову маску підтримуваних функцій
