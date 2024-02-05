---
navigation:
  - sync.constants.md: « Зумовлені константи
  - syncmutex.construct.md: 'SyncMutex::\_\_construct »'
  - index.md: PHP Manual
  - book.sync.md: Sync
title: Клас SyncMutex
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас SyncMutex

(PECL sync >= 1.0.0)

## Вступ

Кросплатформова, нативна реалізація іменованих та безіменних рахункових об'єктів м'ютексу.

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

-   [SyncMutex::\_\_construct](syncmutex.construct.md)— Створює новий об'єкт SyncMutex
-   [SyncMutex::lock](syncmutex.lock.md)— Чекає на ексклюзивне блокування
-   [SyncMutex::unlock](syncmutex.unlock.md) \- Розблокує м'ютекс
