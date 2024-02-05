---
navigation:
  - syncsharedmemory.read.md: '« SyncSharedMemory::read'
  - syncsharedmemory.write.md: 'SyncSharedMemory::write »'
  - index.md: PHP Manual
  - class.syncsharedmemory.md: SyncSharedMemory
title: 'SyncSharedMemory::size'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncSharedMemory::size

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

**Приклад #1 Приклад використання** SyncSharedMemory::size()\*\*\*\*

```php
<?php
$mem = new SyncSharedMemory("AppReportName", 1024);
var_dump($mem->size());
?>
```

Висновок наведеного прикладу буде схожим на:

```
int(1024)
```

### Дивіться також

-   [SyncSharedMemory::\_\_construct()](syncsharedmemory.construct.md) \- Створює новий об'єкт SyncSharedMemory
-   [SyncSharedMemory::write()](syncsharedmemory.write.md) \- Копіює дані в іменовану пам'ять, що розділяється.
-   [SyncSharedMemory::read()](syncsharedmemory.read.md) \- Копіює дані з іменованої пам'яті, що розділяється
