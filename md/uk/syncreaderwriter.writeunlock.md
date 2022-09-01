---
navigation:
  - syncreaderwriter.writelock.html: '« SyncReaderWriter::writelock'
  - class.syncsharedmemory.html: SyncSharedMemory »
  - index.html: PHP Manual
  - class.syncreaderwriter.html: SyncReaderWriter
title: 'SyncReaderWriter::writeunlock'
---
# SyncReaderWriter::writeunlock

(PECL sync >= 1.0.0)

SyncReaderWriter::writeunlock — Знімає блокування запису

### Опис

```methodsynopsis
public SyncReaderWriter::writeunlock(): bool
```

Знімає блокування запису об'єкта [SyncReaderWriter](class.syncreaderwriter.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncReaderWriter::writeunlock()****

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->writelock();
/* ... */
$readwrite->writeunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::writelock()](syncreaderwriter.writelock.html) - Чекає на ексклюзивне блокування запису
