Клас EvPrepare

-   [« EvPeriodic::set](evperiodic.set.html)
    
-   [EvPrepare::\_\_construct »](evprepare.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ev](book.ev.html)
    
-   Клас EvPrepare
    

# Клас EvPrepare

(PECL ev >= 0.2.0)

## Вступ

Спостерігачі **EvPrepare** і [EvCheck](class.evcheck.html) зазвичай використовуються у парі. Спостерігач **EvPrepare** викликається до блокування процесу, потім викликається [EvCheck](class.evcheck.html)

Не дозволяється викликати [EvLoop::run()](evloop.run.html) або аналогічні методи чи функції, введені в поточний цикл подій іншими спостерігачами **EvPrepare** або [EvCheck](class.evcheck.html). Однак інші цикли подій, які не поточні, можуть. Сенс у цьому, що поточному не потрібно перевіряти рекурсію у таких спостерігачах, тобто. завжди буде послідовність: **EvPrepare** -> блокування -> [EvCheck](class.evcheck.html), так що спостерігача кожного виду завжди будуть викликати в парах, захоплюючи блокуючий виклик.

Основна мета полягає в інтеграції інших подійових механізмів у *libev* та покращене їх використання. Вони можуть бути використані, наприклад, при відстеженні зміні змінних, при реалізації спостерігачів, при інтегруванні NET-SNMP або співпрограм бібліотеки і багато іншого. Вони також іноді корисні при кешуванні даних та при очищенні даних до блокування.

Рекомендується встановлювати спостерігачам [EvCheck](class.evcheck.html) найвищий пріоритет (**`Ev::MAXPRI`**), щоб забезпечити можливість їх запуску раніше за будь-які інші спостерігачі після опитування (це не має значення для спостерігачів **EvPrepare**

Крім того, спостерігачі [EvCheck](class.evcheck.html) не зможуть активувати/подавати події. Бувай *libev* повністю підтримує все це, вони можуть виконуватися раніше, ніж інші спостерігачі [EvCheck](class.evcheck.html) виконають свою роботу.

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

-   [EvPrepare::\_\_construct](evprepare.construct.html) - Конструктор спостерігача EvPrepare
-   [EvPrepare::createStopped](evprepare.createstopped.html) - Створити об'єкт класу EvPrepare, але не стартувати його