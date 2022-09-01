---
navigation:
  - parallel-sync.wait.html: '« parallelSync::wait'
  - parallel-sync.invoke.html: 'parallelSync::invoke »'
  - index.md: PHP Manual
  - class.parallel-sync.html: parallelSync
title: 'parallelSync::notify'
---
# parallelSync::notify

parallelSync::notify — Синхронізація

### Опис

```methodsynopsis
public parallel\Sync::notify(bool $all = ?)
```

Повідомляє один (за замовчуванням) або всі потоки, які очікують на об'єкт синхронізації.
