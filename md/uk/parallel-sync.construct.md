---
navigation:
  - class.parallel-sync.html: « parallelSync
  - parallel-sync.get.html: 'parallelSync::get »'
  - index.md: PHP Manual
  - class.parallel-sync.html: parallelSync
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
