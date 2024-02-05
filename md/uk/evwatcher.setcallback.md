---
navigation:
  - evwatcher.keepalive.md: '« EvWatcher::keepalive'
  - evwatcher.start.md: 'EvWatcher::start »'
  - index.md: PHP Manual
  - class.evwatcher.md: EvWatcher
title: 'EvWatcher::setCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvWatcher::setCallback

(PECL ev >= 0.2.0)

EvWatcher::setCallback — Встановлює нову callback-функцію для спостерігача

### Опис

```methodsynopsis
public
   EvWatcher::setCallback(
    callable
     $callback
   ): void
```

Встановлює нову callback-функцію для спостерігача

### Список параметрів

`callback`

Смотрите[callback-функції спостерігачів](ev.watcher-callbacks.md)

### Значення, що повертаються

Функція не повертає значення після виконання.
