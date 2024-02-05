---
navigation:
  - evwatcher.getloop.md: '« EvWatcher::getLoop'
  - evwatcher.keepalive.md: 'EvWatcher::keepalive »'
  - index.md: PHP Manual
  - class.evwatcher.md: EvWatcher
title: 'EvWatcher::invoke'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvWatcher::invoke

(PECL ev >= 0.2.0)

EvWatcher::invoke — Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій

### Опис

```methodsynopsis
public
   EvWatcher::invoke(
    int
     $revents
   ): void
```

Викликає callback-функцію спостерігача із заданою бітовою маскою прийнятих подій.

### Список параметрів

`revents`

Бітова маска спостерігача [прийнятих подій](class.ev.md#ev.constants.watcher-revents)

### Значення, що повертаються

Функція не повертає значення після виконання.
