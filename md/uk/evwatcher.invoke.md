---
navigation:
  - evwatcher.getloop.md: '« EvWatcher::getLoop'
  - evwatcher.keepalive.md: 'EvWatcher::keepalive »'
  - index.md: PHP Manual
  - class.evwatcher.md: EvWatcher
title: 'EvWatcher::invoke'
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

Бітова маска спостерігача [прийнятих подій](class.ev.html#ev.constants.watcher-revents)

### Значення, що повертаються

Функція не повертає значення після виконання.
