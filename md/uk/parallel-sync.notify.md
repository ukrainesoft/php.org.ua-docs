---
navigation:
  - parallel-sync.wait.md: '« parallel\\Sync::wait'
  - parallel-sync.invoke.md: 'parallel\\Sync::\_\_invoke »'
  - index.md: PHP Manual
  - class.parallel-sync.md: parallel\\Sync
title: 'parallel\\Sync::notify'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Sync::notify

(1.1.0)

parallel\\Sync::notify — Синхронізація

### Опис

```methodsynopsis
public parallel\Sync::notify(bool $all = ?)
```

Повідомляє один (за замовчуванням) або всі потоки, які очікують на об'єкт синхронізації.
