---
navigation:
  - syncsharedmemory.construct.md: '« SyncSharedMemory::construct'
  - syncsharedmemory.read.md: 'SyncSharedMemory::read »'
  - index.md: PHP Manual
  - class.syncsharedmemory.md: SyncSharedMemory
title: 'SyncSharedMemory::first'
---
# SyncSharedMemory::first

(PECL sync >= 1.1.0)

SyncSharedMemory::first — Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.

### Опис

```methodsynopsis
public SyncSharedMemory::first(): bool
```

Отримує загальносистемний статус першого екземпляра об'єкта [SyncSharedMemory](class.syncsharedmemory.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncSharedMemory::first()****

```php
<?php
$mem = new SyncSharedMemory("AppReportName", 1024);
if ($mem->first())
{
    // Do first time initialization work here.
}

var_dump($mem->first());

$mem2 = new SyncSharedMemory("AppReportName", 1024);

var_dump($mem2->first());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
bool(true)
bool(false)
```

### Дивіться також

-   [SyncSharedMemory::write()](syncsharedmemory.write.md) - Копіює дані в іменовану пам'ять, що розділяється.
-   [SyncSharedMemory::read()](syncsharedmemory.read.md) - Копіює дані з іменованої пам'яті, що розділяється
