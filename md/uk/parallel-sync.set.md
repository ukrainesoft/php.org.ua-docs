---
navigation:
  - parallel-sync.get.md: '« parallelSync::get'
  - parallel-sync.wait.md: 'parallelSync::wait »'
  - index.md: PHP Manual
  - class.parallel-sync.md: parallelSync
title: 'parallelSync::set'
---
# parallelSync::set

parallelSync::set — Доступ

### Опис

```methodsynopsis
public parallel\Sync::set(scalar $value)
```

Атомарно встановлює значення синхронізації об'єкта.

### Помилки

**Увага**

Викидає parallelSyncErrorIlegallegalValue, якщо `value` не є скалярним значенням.
