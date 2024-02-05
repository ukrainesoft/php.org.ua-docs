---
navigation:
  - evperiodic.set.md: '« EvPeriodic::set'
  - evprepare.construct.md: 'EvPrepare::\_\_construct »'
  - index.md: PHP Manual
  - book.ev.md: Ev
title: Клас EvPrepare
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EvPrepare

(PECL ev >= 0.2.0)

## Вступ

Спостерігачі **EvPrepare**и[EvCheck](class.evcheck.md) зазвичай використовуються у парі. Спостерігач **EvPrepare** викликається до блокування процесу, потім викликається [EvCheck](class.evcheck.md)

Не дозволяється викликати [EvLoop::run()](evloop.run.md) або аналогічні методи чи функції, введені в поточний цикл подій іншими спостерігачами **EvPrepare**или[EvCheck](class.evcheck.md). Однак інші цикли подій, які не поточні, можуть. Сенс у цьому, що поточному не потрібно перевіряти рекурсію у таких спостерігачах, тобто. завжди буде послідовність: **EvPrepare** -> блокування -> [EvCheck](class.evcheck.md), так що спостерігача кожного виду завжди будуть викликати в парах, захоплюючи блокуючий виклик.

Основна мета полягає в інтеграції інших подійових механізмів у *libev* та покращене їх використання. Вони можуть бути використані, наприклад, при відстеженні зміні змінних, при реалізації спостерігачів, при інтегруванні NET-SNMP або співпрограм бібліотеки і багато іншого. Вони також іноді корисні при кешуванні даних та при очищенні даних до блокування.

Рекомендується встановлювати спостерігачам [EvCheck](class.evcheck.md) найвищий пріоритет (**`Ev::MAXPRI`**), щоб забезпечити можливість їх запуску раніше за будь-які інші спостерігачі після опитування (це не має значення для спостерігачів **EvPrepare**

Крім того, спостерігачі [EvCheck](class.evcheck.md) не зможуть активувати/подавати події. Бувай *libev* повністю підтримує все це, вони можуть виконуватися раніше, ніж інші спостерігачі [EvCheck](class.evcheck.md) виконають свою роботу.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvPrepare
     
     
      extends
       EvWatcher
     
     {
    
    
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
    string
     $callback
   , 
    string
     $data
    = ?, 
    string
     $priority
    = ?)

    final
   public
   static
   createStopped(
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

## Зміст

-   [EvPrepare::\_\_construct](evprepare.construct.md) \- Конструктор спостерігача EvPrepare
-   [EvPrepare::createStopped](evprepare.createstopped.md) \- Створити об'єкт класу EvPrepare, але не стартувати його
