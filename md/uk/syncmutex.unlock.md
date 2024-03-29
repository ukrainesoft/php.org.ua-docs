---
navigation:
  - syncmutex.lock.md: '« SyncMutex::lock'
  - class.syncsemaphore.md: SyncSemaphore »
  - index.md: PHP Manual
  - class.syncmutex.md: SyncMutex
title: 'SyncMutex::unlock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncMutex::unlock

(PECL sync >= 1.0.0)

SyncMutex::unlock — Розблокує м'ютекс

### Опис

```methodsynopsis
public SyncMutex::unlock(bool $all = false): bool
```

Зменшує внутрішній лічильник об'єкта [SyncMutex](class.syncmutex.md). Коли внутрішній лічильник досягає нуля, фактичне блокування об'єкта знімається.

### Список параметрів

`all`

Визначає, чи встановлювати внутрішній лічильник на нуль і, отже, знімати блокування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SyncMutex::unlock()\*\*\*\*

```php
<?php
$mutex = new SyncMutex("UniqueName");

$mutex->lock();

/* ... */

$mutex->unlock();
?>
```

### Дивіться також

-   [SyncMutex::lock()](syncmutex.lock.md) \- Чекає на ексклюзивне блокування
