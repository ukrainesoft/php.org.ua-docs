---
navigation:
  - event.timer.md: '« Event::timer'
  - eventbase.construct.md: 'EventBase::\_\_construct »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventBase
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EventBase

(PECL event >= 1.2.6-beta)

## Вступ

Класс**EventBase** представляє структуру подієвої бази якнайбільше. Він містить набір подій і може опитувати їх для визначення, які з них активні.

Кожна подієва база має *метод*или*бекенд*, які використовуються визначення готових подій. Використовувані методи: `select` `poll` `epoll` `kqueue` `devpoll` `evport`и`win32`

Для налаштування подійної бази або для виключення певних бекендів можна використовувати клас [EventConfig](class.eventconfig.md)

**Увага**

*НЕ* руйнуйте об'єкт **EventBase** доки не звільнені пов'язані з `Event` ресурси. В іншому випадку це призведе до непередбачуваних результатів!

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventBase
     
     {
    
    /* Константы */
    
     const
     int
      LOOP_ONCE = 1;

    const
     int
      LOOP_NONBLOCK = 2;

    const
     int
      NOLOCK = 1;

    const
     int
      STARTUP_IOCP = 4;

    const
     int
      NO_CACHE_TIME = 8;

    const
     int
      EPOLL_USE_CHANGELIST = 16;

    /* Методы */
    
   public
   __construct(
    EventConfig
     $cfg
    = ?)
public
   dispatch(): void
public
   exit(
    float
     $timeout
    = ?): bool
public
   free(): void
public
   getFeatures(): int
public
   getMethod(): string
public
   getTimeOfDayCached(): float
public
   gotExit(): bool
public
   gotStop(): bool
public
   loop(
    int
     $flags
    = ?): bool
public
   priorityInit(
    int
     $n_priorities
   ): bool
public
   reInit(): bool
public
   stop(): bool

   }
```

## Обумовлені константи

**`EventBase::LOOP_ONCE`**

Прапор використовується з методом [EventBase::loop()](eventbase.loop.md) і означає: "блокувати, поки libevent не отримає активну подію, а потім вийти після завершення функції зворотного виклику для всіх активних подій".

**`EventBase::LOOP_NONBLOCK`**

Прапор використовується з методом [EventBase::loop()](eventbase.loop.md) і означає: "не блокувати: подивитися, які події вже готові, запустити зворотні виклики із найвищим пріоритетом, потім вийти".

**`EventBase::NOLOCK`**

Прапор конфігурації. Не виділяти блокування для бази подій, навіть якщо блокування налаштовано.

**`EventBase::STARTUP_IOCP`**

Прапор конфігурації лише для Windows. Дозволяє диспетчер IOCP під час старту.

**`EventBase::NO_CACHE_TIME`**

Прапор конфігурації. Замість перевірки поточного часу щоразу, коли цикл готовий запустити функцію зворотного виклику за таймером, перевіряти його після кожного виклику такої функції.

**`EventBase::EPOLL_USE_CHANGELIST`**

Якщо використовується бекенд `epoll` Цей прапор повідомляє, що можна безпечно використовувати внутрішній код списку змін Libevent для пакетного додавання та видалення з метою мінімізації кількості системних викликів.

Встановлення цього прапора може підвищити продуктивність, але може призвести до прояву бага Linux: не безпечно використовувати цей прапор, якщо будь-який із файлових дескрипторів був клонований за допомогою dup() або його аналогів. Може призвести до дивних помилок, що важко діагностуються.

Цей прапор також може бути активований установкою змінного оточення `EVENT_EPOLL_USE_CHANGELIST`

Цей прапор не діє, якщо ви використовуєте будь-який бекенд, крім `epoll`

## Зміст

-   [EventBase::\_\_construct](eventbase.construct.md) \- Конструктор об'єкта EventBase
-   [EventBase::dispatch](eventbase.dispatch.md)— Відправляє події, що очікують.
-   [EventBase::exit](eventbase.exit.md)— Припиняє надсилання подій
-   [EventBase::free](eventbase.free.md)— Визволяє ресурси, виділені для цієї бази подій
-   [EventBase::getFeatures](eventbase.getfeatures.md)— Повертає бітову маску підтримуваних функцій
-   [EventBase::getMethod](eventbase.getmethod.md)— Повертає метод події, що використовується.
-   [EventBase::getTimeOfDayCached](eventbase.gettimeofdaycached.md)— Повертає поточний час базові події
-   [EventBase::gotExit](eventbase.gotexit.md)— Перевіряє, чи було завершено цикл обробки подій.
-   [EventBase::gotStop](eventbase.gotstop.md)— Перевіряє, чи було завершено цикл обробки подій.
-   [EventBase::loop](eventbase.loop.md)— Відправлення очікуваних подій
-   [EventBase::priorityInit](eventbase.priorityinit.md)— Встановлює кількість пріоритетів на основі подій.
-   [EventBase::reInit](eventbase.reinit.md) \- Повторна ініціалізація бази подій (після розгалуження)
-   [EventBase::stop](eventbase.stop.md)— повідомляє event\_base припинити відправку подій
