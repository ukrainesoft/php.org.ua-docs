---
navigation:
  - syncsemaphore.lock.md: '« SyncSemaphore::lock'
  - class.syncevent.md: SyncEvent »
  - index.md: PHP Manual
  - class.syncsemaphore.md: SyncSemaphore
title: 'SyncSemaphore::unlock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncSemaphore::unlock

(PECL sync >= 1.0.0)

Sync Semaphore::unlock — Збільшує рахунок семафору

### Опис

```methodsynopsis
public SyncSemaphore::unlock(int &$prevcount = ?): bool
```

Збільшує рахунок об'єкту [SyncSemaphore](class.syncsemaphore.md)

### Список параметрів

`prevcount`

Повертає попереднє значення лічильника семафору.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SyncSemaphore::unlock()\*\*\*\*

```php
<?php
$semaphore = new SyncSemaphore("LimitedResource_2clients", 2);

if (!$semaphore->lock(3000))
{
    echo "Невозможно заблокировать семафор.";

    exit();
}

/* ... */

$semaphore->unlock();
?>
```

### Дивіться також

-   [SyncSemaphore::lock()](syncsemaphore.lock.md) \- Зменшує рахунок семафора або чекає
