---
navigation:
  - eventbase.gotstop.md: '« EventBase::gotStop'
  - eventbase.priorityinit.md: 'EventBase::priorityInit »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::loop'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBase::loop

(PECL event >= 1.2.6-beta)

EventBase::loop — Надсилання очікуваних подій

### Опис

```methodsynopsis
public
   EventBase::loop(
    int
     $flags
    = ?): bool
```

Очікує, доки події стануть активними, і запускає їх callback-функції.

**Увага**

*НЕ* руйнуйте об'єкт [EventBase](class.eventbase.md) доки не звільнені пов'язані з `Event` ресурси. В іншому випадку це призведе до непередбачуваних результатів!

### Список параметрів

`flags`

Необов'язкові прапори. Одна з констант `EventBase::LOOP_*`Смотрите[EventBase константи](class.eventbase.md#eventbase.constants)

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBase::dispatch()](eventbase.dispatch.md) \- Відправляє очікувані події
