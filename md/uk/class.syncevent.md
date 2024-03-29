---
navigation:
  - syncsemaphore.unlock.md: '« SyncSemaphore::unlock'
  - syncevent.construct.md: 'SyncEvent::\_\_construct »'
  - index.md: PHP Manual
  - book.sync.md: Sync
title: Клас SyncEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [SyncEvent::\_\_construct](syncevent.construct.md)— Створює новий об'єкт SyncEvent
-   [SyncEvent::fire](syncevent.fire.md)— Запускає/встановлює подію
-   [SyncEvent::reset](syncevent.reset.md)— скидає ручну подію
-   [SyncEvent::wait](syncevent.wait.md)— Чекає на запуск/установку події
