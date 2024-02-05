---
navigation:
  - event.constructing.signal.events.md: « Створення подій для сигналів
  - event.add.md: 'Event::add »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас Event
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас Event

(PECL event >= 1.2.6-beta)

## Вступ

Класс**Event** представляє та спрацьовує на наступні події: файловий дескриптор готовий до читання чи запису; стає готовим до читання або запису (тільки edge-triggered I/O (одноразове спрацьовування)); закінчується очікування; отримано системний сигнал; відбулася користувальницька подія.

Кожна подія пов'язана з [EventBase](class.eventbase.md) . Однак подія не буде оброблена, доки не буде *додано*с помощью метода[Event::add()](event.add.md). Додана подія знаходиться у статусі очікування *pending*, Доки воно не відбулося. Після цього воно переходить у статус активно (*active*). Для обробки подій користувач може зареєструвати функцію зворотного дзвінка, яка буде викликана в момент переходу на активний статус. Якщо подія налаштована як постійна (*persistent*), воно повернеться у статус очікування. Якщо воно не постійне, воно вийде з режиму очікування після запуску функції зворотного дзвінка. Метод [Event::del()](event.del.md) *видаляє*відповідно виводячи його зі статусу очікування. Додати його за новою можна за допомогою методу [Event::add()](event.add.md)

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class Event
     
     {
    
    /* Константы */
    
     const
     int
      ET = 32;

    const
     int
      PERSIST = 16;

    const
     int
      READ = 2;

    const
     int
      WRITE = 4;

    const
     int
      SIGNAL = 8;

    const
     int
      TIMEOUT = 1;

    /* Свойства */
    public
     readonly
     bool
      $pending;

    /* Методы */
    
   public
   add(
    float
     $timeout
    = ?): bool
public
   __construct(    
    EventBase
     $base
   ,    
    mixed
     $fd
   ,    
    int
     $what
   ,    
    callable
     $cb
   ,    
    mixed
     $arg
     = NULL
   )
public
   del(): bool
public
   free(): void
public
   static
   getSupportedMethods(): array
public
   pending(
    int
     $flags
   ): bool
public
   set(    
    EventBase
     $base
   ,    
    mixed
     $fd
   ,    
    int
     $what
    = ?,    
    callable
     $cb
    = ?,    
    mixed
     $arg
    = ?): bool
public
   setPriority(
    int
     $priority
   ): bool
public
   setTimer(
    EventBase
     $base
   , 
    callable
     $cb
   , 
    mixed
     $arg
    = ?): bool
public
   static
   signal(    
    EventBase
     $base
   ,    
    int
     $signum
   ,    
    callable
     $cb
   ,    
    mixed
     $arg
    = ?): Event
public
   static
   timer(
    EventBase
     $base
   , 
    callable
     $cb
   , 
    mixed
     $arg
    = ?): Event

   }
```

## Властивості

pending

Позначає, що подія може очікувати. Дивіться [Про постійні події](event.persistence.md)

## Обумовлені константи

**`Event::ET`**

Означає, що подія повинна спрацьовувати один раз при зміні статусу (edge-triggered), якщо бекенд, що використовується, підтримує таку поведінку. Це впливає на семантику **`Event::READ`**и**`Event::WRITE`**

**`Event::PERSIST`**

Позначає, що подія стала. Дивіться [Про постійні події](event.persistence.md)

**`Event::READ`**

Цей прапор вказує на подію, яка стає активною, коли наданий файл (зазвичай потоковий ресурс або сокет) готовий до читання.

**`Event::WRITE`**

Цей прапор вказує на подію, яка стає активною, коли наданий файл (зазвичай потоковий ресурс або сокет) готовий до запису.

**`Event::SIGNAL`**

Використовується для відстеження системних сигналів. Дивіться "Створення подій для сигналів" нижче.

**`Event::TIMEOUT`**

Прапор означає, що активувалася подія після закінчення очікування (timeout).

Флаг\*\*`Event::TIMEOUT`\*\* ігнорується при створенні події: його можна встановити за *додаванні*. Він задається в аргументі `$what` функції зворотного дзвінка, якщо відбулася подія цього типу.

## Зміст

-   [Event::add](event.add.md)— Перевести подію у стан очікування
-   [Event::addSignal](event.addsignal.md) \- Псевдонім Event:: add
-   [Event::addTimer](event.addtimer.md) \- Псевдонім Event:: add
-   [Event::\_\_construct](event.construct.md) \- Конструктор об'єкта Event
-   [Event::del](event.del.md) \- Перевести подію в пасивний стан
-   [Event::delSignal](event.delsignal.md) \- Псевдонім Event::del
-   [Event::delTimer](event.deltimer.md) \- Псевдонім Event::del
-   [Event::free](event.free.md)— Перевести подію в пасивний стан та звільнити всі виділені для неї ресурси
-   [Event::getSupportedMethods](event.getsupportedmethods.md)— Отримати масив з іменами методів, які підтримуються в поточній версії Libevent
-   [Event::pending](event.pending.md)— Перевірити, що подія перебуває у стані очікування або що вона запланована
-   [Event::set](event.set.md) \- Переконфігурувати подію
-   [Event::setPriority](event.setpriority.md) \- Задати пріоритет події
-   [Event::setTimer](event.settimer.md) \- Переконфігурація події таймера
-   [Event::signal](event.signal.md) \- Створити об'єкт події сигналу
-   [Event::timer](event.timer.md) \- Створити об'єкт події таймера
