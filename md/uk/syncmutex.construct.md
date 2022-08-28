Створює новий об'єкт SyncMutex

-   [« SyncMutex](class.syncmutex.html)
    
-   [SyncMutex::lock »](syncmutex.lock.html)
    
-   [PHP Manual](index.html)
    
-   [SyncMutex](class.syncmutex.html)
    
-   Створює новий об'єкт SyncMutex
    

# SyncMutex::construct

(PECL sync >= 1.0.0)

SyncMutex::construct — Створення нового об'єкту SyncMutex

### Опис

```methodsynopsis
public SyncMutex::__construct(string $name = ?)
```

Створює іменований чи безіменний лічильний м'ютекс.

### Список параметрів

`name`

Ім'я мьютексу, якщо це названий об'єкт мьютексу.

> **Зауваження**
> 
> Якщо ім'я вже існує, воно має бути доступним для відкриття поточним користувачем, від імені якого запущено процес, інакше буде викинуто виняток із безглуздим повідомленням про помилку.

### Значення, що повертаються

Новий об'єкт [SyncMutex](class.syncmutex.html)

### Помилки

Якщо м'ютекс не може бути створений або відкритий, викидається виняток.

### Приклади

**Приклад #1 Приклад використання **SyncMutex::construct()** для створення іменованого м'ютексу з часом очікування**

```php
<?php
$mutex = new SyncMutex("UniqueName");

if (!$mutex->lock(3000))
{
    echo "Невозможно создать мьютеккс.";

    exit();
}

/* ... */

$mutex->unlock();
?>
```

**Приклад #2 Приклад використання **SyncMutex::construct()** для створення безіменного м'ютексу**

```php
<?php
$mutex = new SyncMutex();

$mutex->lock();

/* ... */

$mutex->unlock();
?>
```

### Дивіться також

-   [SyncMutex::lock()](syncmutex.lock.html) - Чекає на ексклюзивне блокування
-   [SyncMutex::unlock()](syncmutex.unlock.html) - Розблокує м'ютекс