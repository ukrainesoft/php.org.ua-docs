---
navigation:
  - syncsharedmemory.read.html: '« SyncSharedMemory::read'
  - syncsharedmemory.write.html: 'SyncSharedMemory::write »'
  - index.html: PHP Manual
  - class.syncsharedmemory.html: SyncSharedMemory
title: 'Sync Shared Memory::size'
---
# Sync Shared Memory::size

(PECL sync >= 1.1.0)

SyncSharedMemory::size — Повертає розмір іменованої пам'яті, що розділяється.

### Опис

```methodsynopsis
public SyncSharedMemory::size(): int
```

Витягує розмір пам'яті об'єкта, що розділяється. [SyncSharedMemory](class.syncsharedmemory.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Ціле число, що містить розмір пам'яті, що розділяється. Це буде той самий розмір, який було передано конструктору.

### Приклади

**Приклад #1 Приклад використання **Sync Shared Memory::size()****

```php
<?php
$mem = new SyncSharedMemory("AppReportName", 1024);
var_dump($mem->size());
?>
```

Результатом виконання цього прикладу буде щось подібне:

```
int(1024)
```

### Дивіться також

-   [SyncSharedMemory::construct()](syncsharedmemory.construct.md) - Створює новий об'єкт SyncSharedMemory
-   [SyncSharedMemory::write()](syncsharedmemory.write.md) - Копіює дані в іменовану пам'ять, що розділяється.
-   [SyncSharedMemory::read()](syncsharedmemory.read.md) - Копіює дані з іменованої пам'яті, що розділяється
