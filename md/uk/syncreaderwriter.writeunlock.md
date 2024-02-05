---
navigation:
  - syncreaderwriter.writelock.md: '« SyncReaderWriter::writelock'
  - class.syncsharedmemory.md: SyncSharedMemory »
  - index.md: PHP Manual
  - class.syncreaderwriter.md: SyncReaderWriter
title: 'SyncReaderWriter::writeunlock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncReaderWriter::writeunlock

(PECL sync >= 1.0.0)

SyncReaderWriter::writeunlock — Знімає блокування запису

### Опис

```methodsynopsis
public SyncReaderWriter::writeunlock(): bool
```

Знімає блокування запису об'єкта [SyncReaderWriter](class.syncreaderwriter.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SyncReaderWriter::writeunlock()\*\*\*\*

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->writelock();
/* ... */
$readwrite->writeunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::writelock()](syncreaderwriter.writelock.md) \- Чекає на ексклюзивне блокування запису
