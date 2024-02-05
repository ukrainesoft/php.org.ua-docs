---
navigation:
  - syncevent.wait.md: '« SyncEvent::wait'
  - syncreaderwriter.construct.md: 'SyncReaderWriter::\_\_construct »'
  - index.md: PHP Manual
  - book.sync.md: Sync
title: Клас SyncReaderWriter
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SyncReaderWriter

(PECL sync >= 1.0.0)

## Вступ

Кросплатформова, нативна реалізація іменованих та безіменних об'єктів читання-запису.

Об'єкт читач-письменник дозволяє багатьом читачам чи одному письменнику отримати доступом до ресурсу. Це ефективне рішення для управління ресурсами, де доступ буде головним чином тільки для читання, але іноді потрібний ексклюзивний доступ для запису.

## Огляд класів

```classsynopsis



    
     
      class SyncReaderWriter
     
     {


    /* Методы */
    
   public __construct(string $name = ?, int $autounlock = 1)
public readlock(int $wait = -1): bool
public readunlock(): bool
public writelock(int $wait = -1): bool
public writeunlock(): bool

   }
```

## Зміст

-   [SyncReaderWriter::\_\_construct](syncreaderwriter.construct.md)— Створює новий об'єкт SyncReaderWriter
-   [SyncReaderWriter::readlock](syncreaderwriter.readlock.md)— Чекає на блокування читання
-   [SyncReaderWriter::readunlock](syncreaderwriter.readunlock.md)— Знімає блокування читання
-   [SyncReaderWriter::writelock](syncreaderwriter.writelock.md)— Чекає на ексклюзивне блокування запису
-   [SyncReaderWriter::writeunlock](syncreaderwriter.writeunlock.md) \- Знімає блокування запису
