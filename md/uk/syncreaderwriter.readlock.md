---
navigation:
  - syncreaderwriter.construct.md: '« SyncReaderWriter::construct'
  - syncreaderwriter.readunlock.md: 'SyncReaderWriter::readunlock »'
  - index.md: PHP Manual
  - class.syncreaderwriter.md: SyncReaderWriter
title: 'SyncReaderWriter::readlock'
---
# SyncReaderWriter::readlock

(PECL sync >= 1.0.0)

SyncReaderWriter::readlock — Очікує блокування читання

### Опис

```methodsynopsis
public SyncReaderWriter::readlock(int $wait = -1): bool
```

Отримує блокування читання об'єкта [SyncReaderWriter](class.syncreaderwriter.md)

### Список параметрів

`wait`

Кількість мілісекунд очікування блокування. Значення -1 нескінченне.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **SyncReaderWriter::readlock()****

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->readlock();
/* ... */
$readwrite->readunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::readunlock()](syncreaderwriter.readunlock.md) - Знімає блокування читання
