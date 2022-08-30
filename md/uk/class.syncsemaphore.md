Клас SyncSemaphore

-   [« SyncMutex::unlock](syncmutex.unlock.html)
    
-   [SyncSemaphore::construct »](syncsemaphore.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Sync](book.sync.html)
    
-   Клас SyncSemaphore
    

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

-   [SyncSemaphore::construct](syncsemaphore.construct.html) — Створює новий об'єкт SyncSemaphore
-   [SyncSemaphore::lock](syncsemaphore.lock.html) — Зменшує рахунок семафора чи чекає
-   [SyncSemaphore::unlock](syncsemaphore.unlock.html) - Збільшує рахунок семафору