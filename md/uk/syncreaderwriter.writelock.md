---
navigation:
  - syncreaderwriter.readunlock.md: '« SyncReaderWriter::readunlock'
  - syncreaderwriter.writeunlock.md: 'SyncReaderWriter::writeunlock »'
  - index.md: PHP Manual
  - class.syncreaderwriter.md: SyncReaderWriter
title: 'SyncReaderWriter::writelock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# SyncReaderWriter::writelock

(PECL sync >= 1.0.0)

SyncReaderWriter::writelock — Очікує ексклюзивного блокування запису

### Опис

```methodsynopsis
public SyncReaderWriter::writelock(int $wait = -1): bool
```

Отримує ексклюзивне блокування запису для об'єкту [SyncReaderWriter](class.syncreaderwriter.md)

### Список параметрів

`wait`

Кількість мілісекунд очікування блокування. Значення -1 нескінченне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**SyncReaderWriter::writelock()\*\*\*\*

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->writelock();
/* ... */
$readwrite->writeunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::writeunlock()](syncreaderwriter.writeunlock.md) \- Знімає блокування запису
