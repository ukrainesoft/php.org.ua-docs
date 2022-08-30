Клас SyncMutex

-   [« Обумовлені константи](sync.constants.html)
    
-   [SyncMutex::construct »](syncmutex.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Sync](book.sync.html)
    
-   Клас SyncMutex
    

# Клас SyncMutex

(PECL sync >= 1.0.0)

## Вступ

Кросплатформова, нативна реалізація іменованих та безіменних лічильних об'єктів мьютексу.

М'ютекс - це об'єкт взаємного виключення, який обмежує доступ до спільного ресурсу (наприклад, файлу) одного екземпляра. Рахункові м'ютекси отримують м'ютекс один раз і внутрішньо відстежують, скільки разів м'ютекс був заблокований. М'ютекс розблокується, коли він виходить з області дії або розблокується стільки разів, скільки він був заблокований.

## Огляд класів

```classsynopsis



    
     
      class SyncMutex
     
     {


    /* Методы */
    
   public __construct(string $name = ?)
public lock(int $wait = -1): bool
public unlock(bool $all = false): bool

   }
```

## Зміст

-   [SyncMutex::construct](syncmutex.construct.html) — Створює новий об'єкт SyncMutex
-   [SyncMutex::lock](syncmutex.lock.html) — Чекає на ексклюзивне блокування
-   [SyncMutex::unlock](syncmutex.unlock.html) - Розблокує м'ютекс