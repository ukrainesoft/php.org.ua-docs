Клас EvIdle

-   [« EvFork::createStopped](evfork.createstopped.html)
    
-   [EvIdle::\_\_construct »](evidle.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ev](book.ev.html)
    
-   Клас EvIdle
    

# Клас EvIdle

(PECL ev >= 0.2.0)

## Вступ

Спостерігачі **EvIdle** викликають події тоді, коли жодні інші події такого ж чи вищого пріоритету не перебувають в очікуванні ([EvPrepare](class.evprepare.html) [EvCheck](class.evcheck.html) та інші спостерігачі **EvIdle** не вважаються за одержувачі *події*

Таким чином, цей процес зайнятий обробкою сокетів або очікувань (або навіть сигналів) такого ж або вищого пріоритету доти, доки він не буде активований. Але коли процес перебуває в режимі очікування (або в черзі лише спостерігачі з нижчим пріоритетом), спостерігачі **EvIdle** будуть викликатися один раз за ітерацію циклу подій - доки не будуть зупинені або доки процесом не будуть отримані нові повідомлення і він не буде зайнятий більш пріоритетними завданнями.

Крім підтримки неблокуючого процесу (корисний у деяких випадках), спостерігачі **EvIdle** є гарним місцем для виконання *"псевдо-фонової обробки"* або затримки обробки даних до того часу, поки цикл подій не обробить всі виняткові події.

Найбільш помітний ефект проявляється в тому, що поки що *сплячі* спостерігачі активні, процес *не* блокуватиметься у процесі очікування нових подій.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvIdle
     
     
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
    mixed
     $data
    = ?, 
    int
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

-   [EvIdle::\_\_construct](evidle.construct.html) - Конструктор спостерігача EvIdle
-   [EvIdle::createStopped](evidle.createstopped.html) — Створити об'єкт класу EvIdle, але не стартувати його