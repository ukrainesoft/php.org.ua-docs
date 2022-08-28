Клас EvChild

-   [« EvCheck::createStopped](evcheck.createstopped.html)
    
-   [EvChild::\_\_construct »](evchild.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Ev](book.ev.html)
    
-   Клас EvChild
    

# Клас EvChild

(PECL ev >= 0.2.0)

## Вступ

Спостерігач **EvChild** викликається тоді, коли процес отримує сигнал **`SIGCHLD`** у відповідь деякі зміни статусу дочірнього елемента (зазвичай коли дочірній процес завершує свою роботу чи виходить із нього). Дозволяється встановлювати спостерігач **`EvChild`** після того, як дочірній потік був відгалужений (що має на увазі, що він повинен був вже завершитися), доки не почалася ітерація циклу подій (або триває зі спостерігача), тобто. розгалуження і потім негайна реєстрація спостерігача для дочірнього елемента є гарною практикою, а розгалуження та реєстрація спостерігача після кількох ітерацій циклу подій або за наступного запуску callback-функції - немає.

Спостерігачів **EvChild** дозволяється реєструвати тільки в *циклі за замовчуванням*

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EvChild
     
     
      extends
       EvWatcher
     
     {
    
    /* Свойства */
    
     public
      $pid;

    public
      $rpid;

    public
      $rstatus;

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
    int
     $pid
   ,    
    bool
     $trace
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

    final
   public
   static
   createStopped(    
    int
     $pid
   ,    
    bool
     $trace
   ,    
    callable
     $callback
   ,    
    mixed
     $data
    = ?,    
    int
     $priority
    = ?): object
public
   set(
    int
     $pid
   , 
    bool
     $trace
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

pid

*Тільки читання*. Ідентифікатор процесу, який слідкує, або **`0`**що означає будь-який ідентифікатор процесу.

rpid

*Тільки читання*. Ідентифікатор процесу, який слідкує за зміною статусу.

rstatus

*Тільки читання*. Статус завершення процесу викликаний rpid.

## Зміст

-   [EvChild::\_\_construct](evchild.construct.html) - Створює об'єкт спостерігач EvChild
-   [EvChild::createStopped](evchild.createstopped.html) — Створює зупинений екземпляр спостерігача EvCheck
-   [EvChild::set](evchild.set.html) - Конфігурування спостерігача