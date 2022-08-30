Клас EventListener

-   [« EventHttpRequest::sendReplyStart](eventhttprequest.sendreplystart.html)
    
-   [EventListener::construct »](eventlistener.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventListener
    

# Клас EventListener

(PECL event >= 1.5.0)

## Вступ

Представляє слухач з'єднання.

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventListener
     
     {
    
    /* Константы */
    
     const
     int
      OPT_LEAVE_SOCKETS_BLOCKING = 1;

    const
     int
      OPT_CLOSE_ON_FREE = 2;

    const
     int
      OPT_CLOSE_ON_EXEC = 4;

    const
     int
      OPT_REUSEABLE = 8;

    const
     int
      OPT_THREADSAFE = 16;

    /* Свойства */
    public
     readonly
     int
      $fd;

    /* Методы */
    
   public
   __construct(    
    EventBase
     $base
   ,    
    callable
     $cb
   ,    
    mixed
     $data
   ,    
    int
     $flags
   ,    
    int
     $backlog
   ,    
    mixed
     $target
   )
public
   disable(): bool
public
   enable(): bool
public
   getBase(): void
public
   static
   getSocketName(
    string
     &$address
   , 
    mixed
     &$port
    = ?): bool
public
   setCallback(
    callable
     $cb
   , 
    mixed
     $arg
     = null
   ): void
public
   setErrorCallback(
    string
     $cb
   ): void

   }
```

## Властивості

фд

Числовий файловий дескриптор для сокету. (Додано в `event-1.6.0`

## Обумовлені константи

**`EventListener::OPT_LEAVE_SOCKETS_BLOCKING`**

за замовчуванням, Libevent перемикає файловий дескриптор або сокет у неблокуючий режим. Цей прапор повідомляє Libevent, що слід залишити їх у режимі блокування.

**`EventListener::OPT_CLOSE_ON_FREE`**

Якщо цей прапор встановлено, слухач з'єднання закриє сокет, коли об'єкт **EventListener** буде знищено.

**`EventListener::OPT_CLOSE_ON_EXEC`**

Якщо цей прапорець встановлений, слухач з'єднання встановить прапор close-on-exec на сокет. Дивіться документацію з `fcntl` і **`FD_CLOEXEC`** для платформи.

**`EventListener::OPT_REUSEABLE`**

На деяких платформах, за замовчуванням, після закриття сокета інші сокети не зможуть прив'язатися до того ж порту, поки не пройде деякий час. Даний прапор говорить Libevent позначати сокет як перевикористовуваний, що дозволить відкривати інші сокети на тому порту після його закриття.

**`EventListener::OPT_THREADSAFE`**

Виділяє блокування для слухача, що дозволяє безпечно використовувати його у багатопотоковому варіанті.

## Зміст

-   [EventListener::construct](eventlistener.construct.html) — Створити новий слухач з'єднання, пов'язаний із базою подій
-   [EventListener::disable](eventlistener.disable.html) — Вимикає подію підключення до об'єкта слухача
-   [EventListener::enable](eventlistener.enable.html) — Включає подію підключення до об'єкта слухача
-   [EventListener::getBase](eventlistener.getbase.html) — Повертає базу подій, пов'язану із слухачем подій
-   [EventListener::getSocketName](eventlistener.getsocketname.html) — Отримує поточну адресу, до якої прив'язаний сокет слухача
-   [EventListener::setCallback](eventlistener.setcallback.html) - Мета setCallback
-   [EventListener::setErrorCallback](eventlistener.seterrorcallback.html) - Встановлює callback-функцію помилки слухача подій