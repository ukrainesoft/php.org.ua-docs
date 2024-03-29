---
navigation:
  - evprepare.createstopped.md: '« EvPrepare::createStopped'
  - evsignal.construct.md: 'EvSignal::\_\_construct »'
  - index.md: PHP Manual
  - book.ev.md: Ev
title: Клас EvSignal
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EvSignal

(PECL ev >= 0.2.0)

## Вступ

Спостерігач **EvSignal** створює подію коли процес отримує чи кілька конкретних сигналів. Оскільки сигнали надходять асинхронно, *libev* намагається з цим боротися і доставляти їх синхронно, тобто аналогічно до всіх інших подій у нормальному режимі обробки.

Обмежень на кількість спостерігачів за тим самим сигналом немає, але тільки в межах одного подієвого циклу. Наприклад, у циклі за замовчуванням працює спостерігач за **`SIGINT`**, а в іншому циклі спостерігач за **`SIGIO`**, але при цьому не можна спостерігати **`SIGINT`** у двох циклах одразу. Ну і за **`SIGCHLD`** можна спостерігати лише у циклі за замовчуванням.

Якщо доступно та підтримується, *libev* встановлює свої обробники з дозволеною поведінкою `SA_RESTART` (або аналогом), тому системні дзвінки не будуть некоректно перериватися. Якщо виникають проблеми із перериванням системних викликів сигналами, всі сигнали можна блокувати у спостерігачі [EvCheck](class.evcheck.md) та розблокувати у спостерігачі [EvPrepare](class.evprepare.md)

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvSignal
     
     
      extends
       EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $signum;

    /* Наследуемые свойства */
    public
      $is_active;
public
      $data;
public
      $is_pending;
public
      $priority;

    /* Методы */
    
   public
   __construct(    
    int
     $signum
   ,    
    callable
     $callback
   ,    
    mixed
     $data
     = null
   ,    
    int
     $priority
     = 0
   )

    final
   public
   static
   createStopped(    
    int
     $signum
   ,    
    callable
     $callback
   ,    
    mixed
     $data
     = null
   ,    
    int
     $priority
     = 0
   ): EvSignal
public
   set(
    int
     $signum
   ): void

    /* Наследуемые методы */
    public
   EvWatcher::clear(): int
public
   EvWatcher::feed(
    int
     $revents
   ): void
public
   EvWatcher::getLoop(): EvLoop
public
   EvWatcher::invoke(
    int
     $revents
   ): void
public
   EvWatcher::keepalive(
    bool
     $value
    = ?): bool
public
   EvWatcher::setCallback(
    callable
     $callback
   ): void
public
   EvWatcher::start(): void
public
   EvWatcher::stop(): void

   }
```

## Властивості

signum

Номер сигналу. Дивіться константи, експортовані модулем *pcntl*Также смотрите страницу руководства`signal(7)`

## Зміст

-   [EvSignal::\_\_construct](evsignal.construct.md) \- Конструктор об'єкта спостерігача EvSignal
-   [EvSignal::createStopped](evsignal.createstopped.md)— Create stopped EvSignal watcher object
-   [EvSignal::set](evsignal.set.md)— Налаштування спостерігача
