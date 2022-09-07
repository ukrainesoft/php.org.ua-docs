---
navigation:
  - evstat.stat.md: '« EvStat::stat'
  - evtimer.again.md: 'EvTimer::again »'
  - index.md: PHP Manual
  - book.ev.md: Єв
title: Клас EvTimer
---
# Клас EvTimer

(PECL ev >= 0.2.0)

## Вступ

Спостерігачі **EvTimer** - це звичайні відносні таймери, які створюють подію за заданий час і, опціонально, періодично повторюють її через задані інтервали часу.

Таймери базуються на реальному часі, тобто якщо задати таймер з повторами раз на годину і скинути системний годинник на *Січень минулого року*, то таймер буде також спрацьовувати через (грубо) годину. "Грубо" тому, що відстежити стрибки часу досить складно, і деякі неточності неминучі.

Callback-функція гарантовано запуститься тільки після того, як пройде перевищення заданого часу очікування (не рівно в той же момент, тому що на системах з годинником з низькою роздільною здатністю можуть спостерігатися невеликі затримки). Якщо кілька таймерів будуть готові спрацювати в ту саму ітерацію подієвого циклу, то callback-функції спостерігачів будуть запущені в порядку часу спрацьовування та з урахуванням пріоритету (але це не працює, якщо callback-функції викликають [EvLoop::run()](evloop.run.md) рекурсивно).

Самі по собі таймери намагаються всіма силами уникнути накопичення помилки, тобто якщо таймер налаштований спрацьовувати кожні **`10`** секунд, то зазвичай він спрацьовує точно з **`10`** секундним інтервалом. Однак якщо скрипт не встигає за таймером, оскільки його робота займає більше **`10`** секунд, то таймер спрацює не частіше одного разу за ітерацію подієвого циклу.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvTimer
     
     
      extends
       EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $repeat;

    public
      $remaining;

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
    float
     $after
   ,    
    float
     $repeat
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

    public
   again(): void
final
   public
   static
   createStopped(    
    float
     $after
   ,    
    float
     $repeat
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
   ): EvTimer
public
   set(
    float
     $after
   , 
    float
     $repeat
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

repeat

Якщо одно \*\*`0.0`\*\*таймер автоматично зупиниться, коли буде перевищено час очікування. Якщо більше нуля, таймер автоматично перейде в режим нескінченного повторення через задані інтервали, поки ви його самостійно не зупините.

remaining

Повертає час, що залишився до спрацювання таймера. Якщо таймер активний, то цей час буде вважатися щодо часу поточного подієвого циклу, а якщо таймер не активний, то він дорівнює сконфігурованому значенню часу очікування.

Тобто після того, як створено екземпляр **EvTimer** з `after` рівним **`5.0`** і `repeat` рівним **`7.0`**, remaining поверне **`5.0`**. Коли таймер запуститься та пройде 1 секунда, remaining поверне **`4.0`**. коли таймер закінчиться і буде перезапущено, буде "грубо" повернуто **`7.0`** (Зазвичай трохи менше, тому що запуск callback-функції займає час) і т.д.

## Зміст

-   [EvTimer::again](evtimer.again.md) - Перезапускає таймер спостерігача
-   [EvTimer::construct](evtimer.construct.md) - Конструктор об'єкта спостерігача EvTimer
-   [EvTimer::createStopped](evtimer.createstopped.md) - Створює зупинений спостерігач EvTimer
-   [EvTimer::set](evtimer.set.md) — Налаштовує спостерігача
