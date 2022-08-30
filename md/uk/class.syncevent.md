Клас SyncEvent

-   [« SyncSemaphore::unlock](syncsemaphore.unlock.md)
    
-   [SyncEvent::construct »](syncevent.construct.md)
    
-   [PHP Manual](index.md)
    
-   [Sync](book.sync.md)
    
-   Клас SyncEvent
    

# Клас SyncEvent

(PECL sync >= 1.0.0)

## Вступ

Кросплатформова, нативна реалізація іменованих та безіменних об'єктів подій. Підтримуються як автоматичні, і ручні об'єкти подій.

Об'єкт події без опитування очікує запуску/установки об'єкта. Один екземпляр чекає на об'єкт події, а інший запускає/встановлює подію. Об'єкти подій корисні там, де інакше тривалий процес міг би опитати ресурс (наприклад, перевірити, чи потрібно обробляти завантажені дані).

## Огляд класів

```classsynopsis



    
     
      class SyncEvent
     
     {


    /* Методы */
    
   public __construct(string $name = ?, bool $manual = false, bool $prefire = false)
public fire(): bool
public reset(): bool
public wait(int $wait = -1): bool

   }
```

## Зміст

-   [SyncEvent::construct](syncevent.construct.md) — Створює новий об'єкт SyncEvent
-   [SyncEvent::fire](syncevent.fire.md) — Запускає/встановлює подію
-   [SyncEvent::reset](syncevent.reset.md) — скидає ручну подію
-   [SyncEvent::wait](syncevent.wait.md) — Чекає на запуск/установку події