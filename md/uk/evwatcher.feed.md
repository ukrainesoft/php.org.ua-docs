---
navigation:
  - evwatcher.construct.html: '« EvWatcher::construct'
  - evwatcher.getloop.html: 'EvWatcher::getLoop »'
  - index.html: PHP Manual
  - class.evwatcher.html: EvWatcher
title: 'EvWatcher::feed'
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

Бітова маска спостерігача [прийнятих подій](class.ev.html#ev.constants.watcher-revents)

### Значення, що повертаються

Функція не повертає значення після виконання.
