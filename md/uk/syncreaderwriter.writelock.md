---
navigation:
  - syncreaderwriter.readunlock.html: '« SyncReaderWriter::readunlock'
  - syncreaderwriter.writeunlock.html: 'SyncReaderWriter::writeunlock »'
  - index.html: PHP Manual
  - class.syncreaderwriter.html: SyncReaderWriter
title: 'SyncReaderWriter::writelock'
---
# SyncReaderWriter::writelock

(PECL sync >= 1.0.0)

SyncReaderWriter::writelock — Очікує ексклюзивного блокування запису

### Опис

```methodsynopsis
public SyncReaderWriter::writelock(int $wait = -1): bool
```

Отримує ексклюзивне блокування запису для об'єкту [SyncReaderWriter](class.syncreaderwriter.html)

### Список параметрів

`wait`

Кількість мілісекунд очікування блокування. Значення -1 нескінченне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncReaderWriter::writelock()****

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->writelock();
/* ... */
$readwrite->writeunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::writeunlock()](syncreaderwriter.writeunlock.html) - Знімає блокування запису
