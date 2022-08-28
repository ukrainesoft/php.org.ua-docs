Клас SyncSharedMemory

-   [« SyncReaderWriter::writeunlock](syncreaderwriter.writeunlock.html)
    
-   [SyncSharedMemory::\_\_construct »](syncsharedmemory.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Sync](book.sync.html)
    
-   Клас SyncSharedMemory
    

# Клас SyncSharedMemory

(PECL sync >= 1.1.0)

## Вступ

Кросплатформова, нативна, узгоджена реалізація іменованих об'єктів загальної пам'яті.

Пам'ять, що спільно використовується, дозволяє двом окремим процесам обмінюватися даними без необхідності в складних каналах або сокетах. Існує кілька реалізацій із загальною пам'яттю для PHP. Іменована спільна пам'ять є альтернативою.

Об'єкти синхронізації (наприклад, SyncMutex) досі потрібні для захисту більшості видів використання спільної пам'яті.

## Огляд класів

```classsynopsis



    
     
      class SyncSharedMemory
     
     {


    /* Методы */
    
   public __construct(string $name, int $size)
public first(): bool
public read(int $start = 0, int $length = ?)
public size(): int
public write(string $string = ?, int $start = 0)

   }
```

## Зміст

-   [SyncSharedMemory::\_\_construct](syncsharedmemory.construct.html) — Створює новий об'єкт SyncSharedMemory
-   [SyncSharedMemory::first](syncsharedmemory.first.html) — Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
-   [SyncSharedMemory::read](syncsharedmemory.read.html) — Копіює дані з іменованої пам'яті, що розділяється
-   [SyncSharedMemory::size](syncsharedmemory.size.html) — Повертає розмір іменованої пам'яті, що розділяється.
-   [SyncSharedMemory::write](syncsharedmemory.write.html) — Копіює дані в іменовану пам'ять, що розділяється.