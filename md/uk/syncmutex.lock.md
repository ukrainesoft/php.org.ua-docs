---
navigation:
  - syncmutex.construct.md: '« SyncMutex::construct'
  - syncmutex.unlock.md: 'SyncMutex::unlock »'
  - index.md: PHP Manual
  - class.syncmutex.md: SyncMutex
title: 'SyncMutex::lock'
---
# SyncMutex::lock

(PECL sync >= 1.0.0)

SyncMutex::lock — Чекає на ексклюзивне блокування

### Опис

```methodsynopsis
public SyncMutex::lock(int $wait = -1): bool
```

Отримує ексклюзивне блокування об'єкту [SyncMutex](class.syncmutex.md). Якщо блокування вже встановлено, внутрішній лічильник збільшується.

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

-   [SyncMutex::unlock()](syncmutex.unlock.md) - Розблокує м'ютекс
