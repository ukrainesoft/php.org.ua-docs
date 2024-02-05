---
navigation:
  - evwatcher.construct.md: '« EvWatcher::\_\_construct'
  - evwatcher.getloop.md: 'EvWatcher::getLoop »'
  - index.md: PHP Manual
  - class.evwatcher.md: EvWatcher
title: 'EvWatcher::feed'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EvWatcher::feed

(PECL ev >= 0.2.0)

EvWatcher::feed — Подає зазначені події у цикл подій

### Опис

```methodsynopsis
public
   EvWatcher::feed(
    int
     $revents
   ): void
```

Подає зазначені події у цикл подій, ніби зазначена подія сталася для спостерігача.

### Список параметрів

`revents`

Бітова маска спостерігача [прийнятих подій](class.ev.md#ev.constants.watcher-revents)

### Значення, що повертаються

Функція не повертає значення після виконання.
