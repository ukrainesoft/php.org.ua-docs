---
navigation:
  - syncreaderwriter.writeunlock.md: '« SyncReaderWriter::writeunlock'
  - syncsharedmemory.construct.md: 'SyncSharedMemory::construct »'
  - index.md: PHP Manual
  - book.sync.md: Sync
title: Клас SyncSharedMemory
---
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

-   [SyncSharedMemory::construct](syncsharedmemory.construct.md) — Створює новий об'єкт SyncSharedMemory
-   [SyncSharedMemory::first](syncsharedmemory.first.md) — Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
-   [SyncSharedMemory::read](syncsharedmemory.read.md) — Копіює дані з іменованої пам'яті, що розділяється
-   [SyncSharedMemory::size](syncsharedmemory.size.md) — Повертає розмір іменованої пам'яті, що розділяється.
-   [SyncSharedMemory::write](syncsharedmemory.write.md) — Копіює дані в іменовану пам'ять, що розділяється.
