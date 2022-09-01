---
navigation:
  - parallel-sync.get.html: '« parallelSync::get'
  - parallel-sync.wait.html: 'parallelSync::wait »'
  - index.html: PHP Manual
  - class.parallel-sync.html: parallelSync
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
