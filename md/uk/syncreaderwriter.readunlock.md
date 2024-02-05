---
navigation:
  - syncreaderwriter.readlock.md: '« SyncReaderWriter::readlock'
  - syncreaderwriter.writelock.md: 'SyncReaderWriter::writelock »'
  - index.md: PHP Manual
  - class.syncreaderwriter.md: SyncReaderWriter
title: 'SyncReaderWriter::readunlock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SyncReaderWriter::readunlock()\*\*\*\*

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->readlock();
/* ... */
$readwrite->readunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::readlock()](syncreaderwriter.readlock.md) \- Чекає на блокування читання
