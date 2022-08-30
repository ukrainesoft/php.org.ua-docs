Клас EvFork

-   [« EvEmbed::sweep](evembed.sweep.html)
    
-   [EvFork::construct »](evfork.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Єв](book.ev.html)
    
-   Клас EvFork
    

# Клас EvFork

(PECL ev >= 0.2.0)

## Вступ

Паралельний процес спостерігача викликається тоді, коли викликається `fork()` (зазвичай тому, що про це повідомили *libev* шляхом виклику [EvLoop::fork()](evloop.fork.html)). Виклик здійснюється до наступного блокування циклом подій та до початку виклику спостерігачів [EvCheck](class.evcheck.html) і лише у дочірньому процесі після розгалуження. Якщо хтось зробить виклик [EvLoop::fork()](evloop.fork.html) у неправильному процесі, обробники розгалуження також будуть викликані.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvFork
     
     
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

-   [EvFork::construct](evfork.construct.html) - Конструктор спостерігача EvFork
-   [EvFork::createStopped](evfork.createstopped.html) - Створити об'єкт класу EvFork, але не стартувати його