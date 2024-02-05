---
navigation:
  - syncreaderwriter.construct.md: '« SyncReaderWriter::\_\_construct'
  - syncreaderwriter.readunlock.md: 'SyncReaderWriter::readunlock »'
  - index.md: PHP Manual
  - class.syncreaderwriter.md: SyncReaderWriter
title: 'SyncReaderWriter::readlock'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.

### Приклади

**Приклад #1 Приклад використання** SyncReaderWriter::readlock()\*\*\*\*

```php
<?php
$readwrite = new SyncReaderWriter("FileCacheLock");
$readwrite->readlock();
/* ... */
$readwrite->readunlock();
?>
```

### Дивіться також

-   [SyncReaderWriter::readunlock()](syncreaderwriter.readunlock.md) \- Знімає блокування читання
