---
navigation:
  - syncmutex.unlock.md: '« SyncMutex::unlock'
  - syncsemaphore.construct.md: 'SyncSemaphore::construct »'
  - index.md: PHP Manual
  - book.sync.md: Sync
title: Клас SyncSemaphore
---
# Клас SyncSemaphore

(PECL sync >= 1.0.0)

## Вступ

Кросплатформова, нативна реалізація іменованих та безіменних об'єктів семафорів.

Семафор обмежує доступ до обмеженого ресурсу обмеженою кількістю екземплярів. Семафори відрізняються від мьютексів тим, що вони можуть дозволити доступ до ресурсу більш ніж одному екземпляру одночасно, тоді як м'ютекс допускає лише один екземпляр за один раз.

## Огляд класів

```classsynopsis



    
     
      class SyncSemaphore
     
     {


    /* Методы */
    
   public __construct(string $name = ?, int $initialval = 1, bool $autounlock = true)
public lock(int $wait = -1): bool
public unlock(int &$prevcount = ?): bool

   }
```

## Зміст

-   [SyncSemaphore::construct](syncsemaphore.construct.md) — Створює новий об'єкт SyncSemaphore
-   [SyncSemaphore::lock](syncsemaphore.lock.md) — Зменшує рахунок семафора чи чекає
-   [SyncSemaphore::unlock](syncsemaphore.unlock.md) - Збільшує рахунок семафору
