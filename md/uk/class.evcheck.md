Клас EvCheck

-   [« Ev::verify](ev.verify.html)
    
-   [EvCheck::\_\_construct »](evcheck.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ev](book.ev.html)
    
-   Клас EvCheck
    

# Клас EvCheck

(PECL ev >= 0.2.0)

## Вступ

Спостерігачі [EvPrepare](class.evprepare.html) і **EvCheck** зазвичай використовуються у парі. Спостерігач [EvPrepare](class.evprepare.html) викликається до блокування процесу, потім викликається **EvCheck**

Не дозволяється викликати [EvLoop::run()](evloop.run.html) або аналогічні методи чи функції, введені в поточний цикл подій іншими спостерігачами [EvPrepare](class.evprepare.html) або **EvCheck**. Однак інші цикли подій, які не поточні, можуть. Сенс у цьому, що поточному не потрібно перевіряти рекурсію у таких спостерігачах, тобто. завжди буде послідовність: [EvPrepare](class.evprepare.html) -> блокування -> **EvCheck**, так що спостерігача кожного виду завжди будуть викликати в парах, захоплюючи блокуючий виклик.

Основна мета полягає в інтеграції інших подійових механізмів у *libev* та покращене їх використання. Вони можуть бути використані, наприклад, при відстеженні зміні змінних, при реалізації спостерігачів, при інтегруванні NET-SNMP або співпрограм бібліотеки і багато іншого. Вони також іноді корисні при кешуванні даних та при очищенні даних до блокування.

Рекомендується встановлювати спостерігачам **EvCheck** найвищий пріоритет (**`Ev::MAXPRI`**), щоб забезпечити можливість їх запуску раніше за будь-які інші спостерігачі після опитування (це не має значення для спостерігачів [EvPrepare](class.evprepare.html)

Крім того, спостерігачі **EvCheck** не зможуть активувати/подавати події. Бувай *libev* повністю підтримує все це, вони можуть виконуватися раніше, ніж інші спостерігачі **EvCheck** виконають свою роботу.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvCheck
     
     
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
    callable
     $callback
   , 
    mixed
     $data
    = ?, 
    int
     $priority
    = ?)

    final
   public
   static
   createStopped(
    string
     $callback
   , 
    string
     $data
    = ?, 
    string
     $priority
    = ?): object

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

-   [EvCheck::\_\_construct](evcheck.construct.html) - Конструктор об'єкта EvCheck
-   [EvCheck::createStopped](evcheck.createstopped.html) — Створює зупинений екземпляр спостерігача EvCheck