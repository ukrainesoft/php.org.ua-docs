Чекає на ексклюзивне блокування

-   [« SyncMutex::construct](syncmutex.construct.html)
    
-   [SyncMutex::unlock »](syncmutex.unlock.html)
    
-   [PHP Manual](index.html)
    
-   [SyncMutex](class.syncmutex.html)
    
-   Чекає на ексклюзивне блокування
    

# SyncMutex::lock

(PECL sync >= 1.0.0)

SyncMutex::lock — Чекає на ексклюзивне блокування

### Опис

```methodsynopsis
public SyncMutex::lock(int $wait = -1): bool
```

Отримує ексклюзивне блокування об'єкту [SyncMutex](class.syncmutex.html). Якщо блокування вже встановлено, внутрішній лічильник збільшується.

### Список параметрів

`wait`

Кількість мілісекунд очікування на ексклюзивне блокування. Значення -1 означає нескінченний час очікування.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncMutex::lock()****

```php
<?php
$mutex = new SyncMutex("UniqueName");

if (!$mutex->lock(3000))
{
    echo "Невозможно заблокировать мьютекс.";

    exit();
}

/* ... */

$mutex->unlock();
?>
```

### Дивіться також

-   [SyncMutex::unlock()](syncmutex.unlock.html) - Розблокує м'ютекс