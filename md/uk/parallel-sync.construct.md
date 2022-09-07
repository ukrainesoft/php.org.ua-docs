---
navigation:
  - class.parallel-sync.md: « parallelSync
  - parallel-sync.get.md: 'parallelSync::get »'
  - index.md: PHP Manual
  - class.parallel-sync.md: parallelSync
title: 'parallelSync::construct'
---
# parallelSync::construct

parallelSync::construct - Конструктор класу

### Опис

```methodsynopsis
public parallel\Sync::__construct()
```

Створює новий об'єкт синхронізації без значення.

```methodsynopsis
public parallel\Sync::__construct(scalar $value)
```

Створює новий об'єкт синхронізації, який містить задане скалярне значення.

### Помилки

**Увага**

Викидає parallelSyncErrorIlegallegalValue, якщо `value` не є скалярним значенням.
