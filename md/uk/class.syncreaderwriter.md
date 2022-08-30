Клас SyncReaderWriter

-   [« SyncEvent::wait](syncevent.wait.html)
    
-   [SyncReaderWriter::construct »](syncreaderwriter.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Sync](book.sync.html)
    
-   Клас SyncReaderWriter
    

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

-   [SyncReaderWriter::construct](syncreaderwriter.construct.html) — Створює новий об'єкт SyncReaderWriter
-   [SyncReaderWriter::readlock](syncreaderwriter.readlock.html) — Чекає на блокування читання
-   [SyncReaderWriter::readunlock](syncreaderwriter.readunlock.html) — Знімає блокування читання
-   [SyncReaderWriter::writelock](syncreaderwriter.writelock.html) — Чекає на ексклюзивне блокування запису
-   [SyncReaderWriter::writeunlock](syncreaderwriter.writeunlock.html) - Знімає блокування запису