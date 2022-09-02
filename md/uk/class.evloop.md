---
navigation:
  - evio.set.md: '« EvIo::set'
  - evloop.backend.md: 'EvLoop::backend »'
  - index.md: PHP Manual
  - book.ev.md: Єв
title: Клас EvLoop
---
# Клас EvLoop

(PECL ev >= 0.2.0)

## Вступ

Представляє подійний цикл, який завжди відрізняється від *циклу за замовчуванням*. На відміну від *циклу за замовчуванням*, він не може працювати зі спостерігачами [EvChild](class.evchild.md)

Якщо доступна робота з потоками виконання, необхідно створити цикл для кожного потоку використовуючи в якості батька *цикл за замовчуванням*

*Типовий цикл за замовчуванням* ініціалізується автоматично за допомогою *Єв*. Він доступний за допомогою методів класу [Єв](class.ev.md) або за допомогою методу [EvLoop::defaultLoop()](evloop.defaultloop.md)

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EvLoop
     
     {
    
    /* Свойства */
    
     public
      $data;

    public
      $backend;

    public
      $is_default_loop;

    public
      $iteration;

    public
      $pending;

    public
      $io_interval;

    public
      $timeout_interval;

    public
      $depth;

    /* Методы */
    
   public
   __construct(    
    int
     $flags
    = ?,    
    mixed
     $data
     = NULL
   ,    
    float
     $io_interval
     = 0.0
   ,    
    float
     $timeout_interval
     = 0.0
   )

    public
   backend(): int
final
   public
   check(
    string
     $callback
   , 
    string
     $data
    = ?, 
    string
     $priority
    = ?): EvCheck
final
   public
   child(    
    string
     $pid
   ,    
    string
     $trace
   ,    
    string
     $callback
   ,    
    string
     $data
    = ?,    
    string
     $priority
    = ?): EvChild
public
   static
   defaultLoop(    
    int
     $flags
     = Ev::FLAG_AUTO
   ,    
    mixed
     $data
     = NULL
   ,    
    float
     $io_interval
     = 0.
   ,    
    float
     $timeout_interval
     = 0.
   ): EvLoop
final
   public
   embed(    
    string
     $other
   ,    
    string
     $callback
    = ?,    
    string
     $data
    = ?,    
    string
     $priority
    = ?): EvEmbed
final
   public
   fork(
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
   ): EvFork
final
   public
   idle(
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
   ): EvIdle
public
   invokePending(): void
final
   public
   io(    
    mixed
     $fd
   ,    
    int
     $events
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
   ): EvIo
public
   loopFork(): void
public
   now(): float
public
   nowUpdate(): void
final
   public
   periodic(    
    float
     $offset
   ,    
    float
     $interval
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
final
   public
   prepare(
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
   ): EvPrepare
public
   resume(): void
public
   run(
    int
     $flags
     = 0
   ): void
final
   public
   signal(    
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
final
   public
   stat(    
    string
     $path
   ,    
    float
     $interval
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
   ): EvStat
public
   stop(
    int
     $how
    = ?): void
public
   suspend(): void
final
   public
   timer(    
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
   verify(): void

   }
```

## Властивості

data

Довільні дані, додані циклу

backend

*Тільки читання*. . [Прапори бекенда](class.ev.md#ev.constants.watcher-backends) що вказують який подійний бекенд використовується.

ісdefaultloop

*Тільки читання*. Якщо **`true`**, Це цикл за замовчуванням.

iteration

Поточний лічильник ітерацій. Дивись [Ev::iteration()](ev.iteration.md)

pending

Кількість спостерігачів, що очікують . **`0`** означає, що спостерігачі, що очікують, відсутні.

іоinterval

Вищі значення iointerval дозволяють *libev* витрачати більше часу для збору подій [EvIo](class.evio.md), що дозволить обробити більше подій за одну ітерацію, заплативши за це збільшеними затримками. Час очікування (і [EvPeriodic](class.evperiodic.md) і [EvTimer](class.evtimer.md)) не буде порушено. Налаштування в ненульове значення додати додатковий виклик `sleep()` більшість ітерацій циклу. Час сну гарантує, що *libev* не передаватиме події [EvIo](class.evio.md) частіше, ніж один раз за цей період, у середньому. Для більшості програм хорошим значенням iointerval буде значення близько **`0.1`**, цього достатньо більшості інтерактивних серверів (не для ігор). Зазвичай ви не помітите жодної різниці, якщо встановите його менше **`0.01`**, так як це значення буде близько до мінімального інтервалу обчислюваного часу для більшості систем.

Також читайте [» ФУНКЦІЇ УПРАВЛІННЯ ПОДІЙНИМИ ЦИКЛАМИ](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS)

timeoutinterval

Вищі значення timeoutinterval дозволять *libev* витрачати більше часу для збору перевищеного часу очікування рахунок збільшення затримок/джиттеров/неточностей (функція зворотного виклику спостерігача буде викликана пізніше). Спостерігачі [EvIo](class.evio.md) не будуть порушені. Збільшення цього значення не викличе перевитрати ресурсів у *libev*. Також читайте [» ФУНКЦІЇ УПРАВЛІННЯ ПОДІЙНИМИ ЦИКЛАМИ](http://pod.tst.eu/http://cvs.schmorp.de/libev/ev.pod#FUNCTIONS_CONTROLLING_EVENT_LOOPS)

depth

Глибина рекурсії. Дивіться [Ev::depth()](ev.depth.md)

## Зміст

-   [EvLoop::backend](evloop.backend.md) — Повертає ціле число, що описує бекенд, який використовується libev
-   [EvLoop::check](evloop.check.md) — Створює об'єкт EvCheck, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::child](evloop.child.md) — Створює об'єкт EvChild, пов'язаний із поточним циклом подій
-   [EvLoop::construct](evloop.construct.md) - Конструктор об'єкта циклу подій
-   [EvLoop::defaultLoop](evloop.defaultloop.md) — Повертає або створює цикл стандартних подій
-   [EvLoop::embed](evloop.embed.md) — Створює екземпляр спостерігача EvEmbed, пов'язаний із поточним об'єктом EvLoop
-   [EvLoop::fork](evloop.fork.md) — Створює об'єкт спостерігача EvFork, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::idle](evloop.idle.md) — Створює об'єкт спостерігача EvIdle, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::invokePending](evloop.invokepending.md) — Викликає всіх спостерігачів, що очікують, при скиданні їх відкладеного стану
-   [EvLoop::io](evloop.io.md) — Створює об'єкт спостерігача EvIo, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::loopFork](evloop.loopfork.md) — Викликається після розгалуження
-   [EvLoop::now](evloop.now.md) - Повертає поточне "event loop time"
-   [EvLoop::nowUpdate](evloop.nowupdate.md) — Встановлює поточний час, запитуючи ядро, оновлюючи час, який повертається EvLoop::now у процесі
-   [EvLoop::periodic](evloop.periodic.md) — Створює об'єкт спостерігача EvPeriodic, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::prepare](evloop.prepare.md) — Створює об'єкт спостерігача EvPrepare, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::resume](evloop.resume.md) — Відновлює раніше зупинений цикл подій
-   [EvLoop::run](evloop.run.md) — Перевіряє події та викликає callback-функції у циклі
-   [EvLoop::signal](evloop.signal.md) — Створює об'єкт спостерігача EvSignal, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::stat](evloop.stat.md) — Створює об'єкт спостерігача EvStat, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::stop](evloop.stop.md) - Зупиняє цикл подій
-   [EvLoop::suspend](evloop.suspend.md) - Припиняє цикл
-   [EvLoop::timer](evloop.timer.md) — Створює об'єкт спостерігача EvTimer, пов'язаний із поточним екземпляром циклу подій
-   [EvLoop::verify](evloop.verify.md) - Виконує внутрішні перевірки узгодженості (для налагодження)
