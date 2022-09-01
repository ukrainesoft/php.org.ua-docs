---
navigation:
  - syncreaderwriter.readlock.md: '« SyncReaderWriter::readlock'
  - syncreaderwriter.writelock.md: 'SyncReaderWriter::writelock »'
  - index.md: PHP Manual
  - class.syncreaderwriter.md: SyncReaderWriter
title: 'SyncReaderWriter::readunlock'
---
# SyncReaderWriter::readunlock

(PECL sync >= 1.0.0)

SyncReaderWriter::readunlock — Знімає блокування читання

### Опис

```methodsynopsis
public SyncReaderWriter::readunlock(): bool
```

Знімає блокування читання об'єкта [SyncReaderWriter](class.syncreaderwriter.md)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncReaderWriter::readunlock()****

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->readlock();
/* ... */
$readwrite->readunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::readlock()](syncreaderwriter.readlock.md) - Чекає на блокування читання
