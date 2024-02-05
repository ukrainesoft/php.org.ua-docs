---
navigation:
  - eventbase.construct.md: '« EventBase::\_\_construct'
  - eventbase.exit.md: 'EventBase::exit »'
  - index.md: PHP Manual
  - class.eventbase.md: EventBase
title: 'EventBase::dispatch'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBase::dispatch

(PECL event >= 1.2.6-beta)

EventBase::dispatch — Відправляє події, що очікують.

### Опис

```methodsynopsis
public
   EventBase::dispatch(): void
```

Очікує, доки події стануть активними, і запускає їх callback-функції. Так само як [EventBase::loop()](eventbase.loop.md) без встановлених прапорів.

**Увага**

*НЕ* руйнуйте об'єкт [EventBase](class.eventbase.md) доки не звільнені пов'язані з `Event` ресурси. В іншому випадку це призведе до непередбачуваних результатів!

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Дивіться також

-   [EventBase::loop()](eventbase.loop.md) \- Відправлення очікуваних подій
