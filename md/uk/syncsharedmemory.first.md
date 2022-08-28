Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.

-   [« SyncSharedMemory::\_\_construct](syncsharedmemory.construct.html)
    
-   [SyncSharedMemory::read »](syncsharedmemory.read.html)
    
-   [PHP Manual](index.html)
    
-   [SyncSharedMemory](class.syncsharedmemory.html)
    
-   Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
    

# SyncSharedMemory::first

(PECL sync >= 1.1.0)

SyncSharedMemory::first — Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.

### Опис

```methodsynopsis
public SyncSharedMemory::first(): bool
```

Отримує загальносистемний статус першого екземпляра об'єкта [SyncSharedMemory](class.syncsharedmemory.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncSharedMemory::first()****

```php
<?php
$mem = new SyncSharedMemory("AppReportName", 1024);
if ($mem->first())
{
    // Do first time initialization work here.
}

var_dump($mem->first());

$mem2 = new SyncSharedMemory("AppReportName", 1024);

var_dump($mem2->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```

### Дивіться також

-   [SyncSharedMemory::write()](syncsharedmemory.write.html) - Копіює дані в іменовану пам'ять, що розділяється.
-   [SyncSharedMemory::read()](syncsharedmemory.read.html) - Копіює дані з іменованої пам'яті, що розділяється