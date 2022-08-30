Sync

-   [« Shmop](class.shmop.html)
    
-   [Введение »](intro.sync.html)
    
-   [PHP Manual](index.html)
    
-   [Модули для управления процессами программ](refs.fileprocess.process.html)
    
-   Sync
    

# Sync

-   [Введение](intro.sync.html)
-   [Установка и настройка](sync.setup.html)
    -   [Требования](sync.requirements.html)
    -   [Установка](sync.installation.html)
    -   [Настройка во время выполнения](sync.configuration.html)
    -   [Типы ресурсов](sync.resources.html)
-   [Предопределённые константы](sync.constants.html)
-   [SyncMutex](class.syncmutex.html) - Клас SyncMutex
    -   [SyncMutex::construct](syncmutex.construct.html) — Створює новий об'єкт SyncMutex
    -   [SyncMutex::lock](syncmutex.lock.html) — Чекає на ексклюзивне блокування
    -   [SyncMutex::unlock](syncmutex.unlock.html) - Розблокує м'ютекс
-   [SyncSemaphore](class.syncsemaphore.html) - Клас SyncSemaphore
    -   [SyncSemaphore::construct](syncsemaphore.construct.html) — Створює новий об'єкт SyncSemaphore
    -   [SyncSemaphore::lock](syncsemaphore.lock.html) — Зменшує рахунок семафора чи чекає
    -   [SyncSemaphore::unlock](syncsemaphore.unlock.html) - Збільшує рахунок семафору
-   [SyncEvent](class.syncevent.html) - Клас SyncEvent
    -   [SyncEvent::construct](syncevent.construct.html) — Створює новий об'єкт SyncEvent
    -   [SyncEvent::fire](syncevent.fire.html) — Запускає/встановлює подію
    -   [SyncEvent::reset](syncevent.reset.html) — скидає ручну подію
    -   [SyncEvent::wait](syncevent.wait.html) — Чекає на запуск/установку події
-   [SyncReaderWriter](class.syncreaderwriter.html) - Клас SyncReaderWriter
    -   [SyncReaderWriter::construct](syncreaderwriter.construct.html) — Створює новий об'єкт SyncReaderWriter
    -   [SyncReaderWriter::readlock](syncreaderwriter.readlock.html) — Чекає на блокування читання
    -   [SyncReaderWriter::readunlock](syncreaderwriter.readunlock.html) — Знімає блокування читання
    -   [SyncReaderWriter::writelock](syncreaderwriter.writelock.html) — Чекає на ексклюзивне блокування запису
    -   [SyncReaderWriter::writeunlock](syncreaderwriter.writeunlock.html) - Знімає блокування запису
-   [SyncSharedMemory](class.syncsharedmemory.html) — Клас SyncSharedMemory
    -   [SyncSharedMemory::construct](syncsharedmemory.construct.html) — Створює новий об'єкт SyncSharedMemory
    -   [SyncSharedMemory::first](syncsharedmemory.first.html) — Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
    -   [SyncSharedMemory::read](syncsharedmemory.read.html) — Копіює дані з іменованої пам'яті, що розділяється.
    -   [SyncSharedMemory::size](syncsharedmemory.size.html) — Повертає розмір іменованої пам'яті, що розділяється.
    -   [SyncSharedMemory::write](syncsharedmemory.write.html) — Копіює дані в іменовану пам'ять, що розділяється.