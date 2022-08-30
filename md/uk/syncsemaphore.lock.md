Зменшує рахунок семафору або чекає

-   [« SyncSemaphore::construct](syncsemaphore.construct.html)
    
-   [SyncSemaphore::unlock »](syncsemaphore.unlock.html)
    
-   [PHP Manual](index.html)
    
-   [SyncSemaphore](class.syncsemaphore.html)
    
-   Зменшує рахунок семафору або чекає
    

# SyncSemaphore::lock

(PECL sync >= 1.0.0)

Sync Semaphore::lock — Зменшує рахунок семафору або чекає

### Опис

```methodsynopsis
public SyncSemaphore::lock(int $wait = -1): bool
```

Зменшує лічильник об'єкта [SyncSemaphore](class.syncsemaphore.html) або чекає, поки семафор стане відмінним від нуля.

### Список параметрів

`wait`

Кількість мілісекунд очікування на семафор. Значення -1 нескінченне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncSemaphore::lock()****

```php
<?php
$semaphore = new SyncSemaphore("LimitedResource_2clients", 2);

if (!$semaphore->lock(3000))
{
    echo "Невозможно заблокировать семафор.";

    exit();
}

/* ... */

$semaphore->unlock();
?>
```

### Дивіться також

-   [SyncSemaphore::unlock()](syncsemaphore.unlock.html) - Збільшує рахунок семафору