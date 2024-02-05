---
navigation:
  - evloop.verify.md: '« EvLoop::verify'
  - evperiodic.again.md: 'EvPeriodic::again »'
  - index.md: PHP Manual
  - book.ev.md: Ev
title: Клас EvPeriodic
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EvPeriodic

(PECL ev >= 0.2.0)

## Вступ

Періодичні спостерігачі також, свого роду, таймери, але набагато непостійніші.

В отличие от[EvTimer](class.evtimer.md) , спостерігачі **EvPeriodic** базуються не на реальному часі (або відносному часі, що фізично пройшов), а на "системному" (тому, що показується на вашому годиннику). Різниця в тому, що такий час може йти швидше або повільніше "реального", або взагалі стрибати, у момент переходу на зимовий/літній час або просто ручної зміни часу.

Спостерігач **EvPeriodic** можна налаштувати на спрацювання після певного часу. Наприклад, якщо спостерігач **EvPeriodic** налаштований спрацювати *"в 10 секунд"*(т.е[EvLoop::now()](evloop.now.md) **`10.0`** секунд за "системним" часом, а не через 10 секунд!) і відразу після цього системний час скинули на *перше січня минулого року*, то спостерігач спрацює через рік або більше, рівно в той момент, коли системний час дорівнюватиме заданому. В той час як [EvTimer](class.evtimer.md) просто спрацює через \*\*`10`\*\*секунд после запуска.

Як і з таймерами, callback-функція гарантовано спрацює після настання необхідного часу. Якщо кілька таймерів будуть готові спрацювати в одній і тій самій ітерації подієвого циклу, то першими спрацюють ті, які повинні працювати раніше за часом. (Це більше не поширюється на ситуації, коли callback-функції рекурсивно викликають [EvLoop::run()](evloop.run.md)

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvPeriodic
     
     
      extends
       EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $offset;

    public
      $interval;

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
     $offset
   ,    
    string
     $interval
   ,    
    callable
     $reschedule_cb
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
public
   at(): float
final
   public
   static
   createStopped(    
    float
     $offset
   ,    
    float
     $interval
   ,    
    callable
     $reschedule_cb
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
   ): EvPeriodic
public
   set(
    float
     $offset
   , 
    float
     $interval
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

offset

При повторенні цей параметр містить значення зсуву, інакше - абсолютний час (значення зсуву передається в [EvPeriodic::set()](evperiodic.set.md), хотя*libev* може його змінити для кращої чисельної стабільності).

interval

Поточне значення інтервалу. Може бути змінено в будь-який час, але зміни набудуть чинності тільки після спрацювання спостерігача або під час виклику [EvPeriodic::again()](evperiodic.again.md)

## Зміст

-   [EvPeriodic::again](evperiodic.again.md)— Зупиняє та знову запускає періодичний спостерігач
-   [EvPeriodic::at](evperiodic.at.md)— Повертає абсолютний час, коли спостерігач запуститься наступного разу
-   [EvPeriodic::\_\_construct](evperiodic.construct.md) \- Конструктор об'єкта спостерігача EvPeriodic
-   [EvPeriodic::createStopped](evperiodic.createstopped.md) \- Створює зупинений спостерігач EvPeriodic
-   [EvPeriodic::set](evperiodic.set.md)— Налаштовує спостерігача
