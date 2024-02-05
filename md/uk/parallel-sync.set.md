---
navigation:
  - parallel-sync.get.md: '« parallel\\Sync::get'
  - parallel-sync.wait.md: 'parallel\\Sync::wait »'
  - index.md: PHP Manual
  - class.parallel-sync.md: parallel\\Sync
title: 'parallel\\Sync::set'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Sync::set

(1.1.0)

parallel\\Sync::set — Доступ

### Опис

```methodsynopsis
public parallel\Sync::set(scalar $value)
```

Атомарно встановлює значення синхронізації об'єкта.

### Помилки

**Увага**

Викидає parallel\\Sync\\Error\\IllegalValue, если`value` не є скалярним значенням.
