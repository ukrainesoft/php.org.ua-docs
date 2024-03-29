---
navigation:
  - class.shmop.md: « Shmop
  - intro.sync.md: Вступ "
  - index.md: PHP Manual
  - refs.fileprocess.process.md: Модулі для керування процесами програм
title: Sync
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Sync

-   [Вступ](intro.sync.md)
-   [Встановлення та налаштування](sync.setup.md)
    -   [Вимоги](sync.requirements.md)
    -   [Установка](sync.installation.md)
    -   [Налаштування під час виконання](sync.configuration.md)
    -   [Типи ресурсів](sync.resources.md)
-   [Обумовлені константи](sync.constants.md)
-   [SyncMutex](class.syncmutex.md) \- Клас SyncMutex
    -   [SyncMutex::\_\_construct](syncmutex.construct.md)— Створює новий об'єкт SyncMutex
    -   [SyncMutex::lock](syncmutex.lock.md)— Чекає на ексклюзивне блокування
    -   [SyncMutex::unlock](syncmutex.unlock.md) \- Розблокує м'ютекс
-   [SyncSemaphore](class.syncsemaphore.md) \- Клас SyncSemaphore
    -   [SyncSemaphore::\_\_construct](syncsemaphore.construct.md)— Створює новий об'єкт SyncSemaphore
    -   [SyncSemaphore::lock](syncsemaphore.lock.md)— Зменшує рахунок семафора чи чекає
    -   [SyncSemaphore::unlock](syncsemaphore.unlock.md) \- Збільшує рахунок семафору
-   [SyncEvent](class.syncevent.md) \- Клас SyncEvent
    -   [SyncEvent::\_\_construct](syncevent.construct.md)— Створює новий об'єкт SyncEvent
    -   [SyncEvent::fire](syncevent.fire.md)— Запускає/встановлює подію
    -   [SyncEvent::reset](syncevent.reset.md)— скидає ручну подію
    -   [SyncEvent::wait](syncevent.wait.md)— Чекає на запуск/установку події
-   [SyncReaderWriter](class.syncreaderwriter.md) \- Клас SyncReaderWriter
    -   [SyncReaderWriter::\_\_construct](syncreaderwriter.construct.md)— Створює новий об'єкт SyncReaderWriter
    -   [SyncReaderWriter::readlock](syncreaderwriter.readlock.md)— Чекає на блокування читання
    -   [SyncReaderWriter::readunlock](syncreaderwriter.readunlock.md)— Знімає блокування читання
    -   [SyncReaderWriter::writelock](syncreaderwriter.writelock.md)— Чекає на ексклюзивне блокування запису
    -   [SyncReaderWriter::writeunlock](syncreaderwriter.writeunlock.md) \- Знімає блокування запису
-   [SyncSharedMemory](class.syncsharedmemory.md)— Клас SyncSharedMemory
    -   [SyncSharedMemory::\_\_construct](syncsharedmemory.construct.md)— Створює новий об'єкт SyncSharedMemory
    -   [SyncSharedMemory::first](syncsharedmemory.first.md)— Перевіряє, чи є об'єкт першим загальносистемним екземпляром іменованої пам'яті, що розділяється.
    -   [SyncSharedMemory::read](syncsharedmemory.read.md)— Копіює дані з іменованої пам'яті, що розділяється
    -   [SyncSharedMemory::size](syncsharedmemory.size.md)— Повертає розмір іменованої пам'яті, що розділяється.
    -   [SyncSharedMemory::write](syncsharedmemory.write.md)— Копіює дані в іменовану пам'ять, що розділяється.
