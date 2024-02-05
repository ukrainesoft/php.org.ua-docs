---
navigation:
  - class.parallel-sync.md: « parallel\\Sync
  - parallel-sync.get.md: 'parallel\\Sync::get »'
  - index.md: PHP Manual
  - class.parallel-sync.md: parallel\\Sync
title: 'parallel\\Sync::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# parallel\\Sync::\_\_construct

(1.1.0)

parallel\\Sync::\_\_construct - Конструктор класу

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

Викидає parallel\\Sync\\Error\\IllegalValue, если`value` не є скалярним значенням.
