Розблокує м'ютекс

-   [« SyncMutex::lock](syncmutex.lock.html)
    
-   [SyncSemaphore »](class.syncsemaphore.html)
    
-   [PHP Manual](index.html)
    
-   [SyncMutex](class.syncmutex.html)
    
-   Розблокує м'ютекс
    

# SyncMutex::unlock

(PECL sync >= 1.0.0)

SyncMutex::unlock — Розблокує м'ютекс

### Опис

```methodsynopsis
public SyncMutex::unlock(bool $all = false): bool
```

Зменшує внутрішній лічильник об'єкта [SyncMutex](class.syncmutex.html). Коли внутрішній лічильник досягає нуля, фактичне блокування об'єкта знімається.

### Список параметрів

`all`

Визначає, чи встановлювати внутрішній лічильник на нуль і, отже, знімати блокування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncMutex::unlock()****

```php
<?php
$mutex = new SyncMutex("UniqueName");

$mutex->lock();

/* ... */

$mutex->unlock();
?>
```

### Дивіться також

-   [SyncMutex::lock()](syncmutex.lock.html) - Чекає на ексклюзивне блокування