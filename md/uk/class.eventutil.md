Клас EventUtil

-   [« EventSslContext::construct](eventsslcontext.construct.md)
    
-   [EventUtil::construct »](eventutil.construct.md)
    
-   [PHP Manual](index.md)
    
-   [Event](book.event.md)
    
-   Клас EventUtil
    

# Клас EventUtil

(PECL event >= 1.5.0)

## Вступ

**EventUtil** - клас синглтон, що містить допоміжні методи та константи.

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventUtil
     
     {
    
    /* Константы */
    
     const
     int
      AF_INET = 2;

    const
     int
      AF_INET6 = 10;

    const
     int
      AF_UNSPEC = 0;

    const
     int
      LIBEVENT_VERSION_NUMBER = 33559808;

    const
     int
      SO_DEBUG = 1;

    const
     int
      SO_REUSEADDR = 2;

    const
     int
      SO_KEEPALIVE = 9;

    const
     int
      SO_DONTROUTE = 5;

    const
     int
      SO_LINGER = 13;

    const
     int
      SO_BROADCAST = 6;

    const
     int
      SO_OOBINLINE = 10;

    const
     int
      SO_SNDBUF = 7;

    const
     int
      SO_RCVBUF = 8;

    const
     int
      SO_SNDLOWAT = 19;

    const
     int
      SO_RCVLOWAT = 18;

    const
     int
      SO_SNDTIMEO = 21;

    const
     int
      SO_RCVTIMEO = 20;

    const
     int
      SO_TYPE = 3;

    const
     int
      SO_ERROR = 4;

    const
     int
      SOL_SOCKET = 1;

    const
     int
      SOL_TCP = 6;

    const
     int
      SOL_UDP = 17;

    const
     int
      IPPROTO_IP = 0;

    const
     int
      IPPROTO_IPV6 = 41;

    /* Методы */
    
   abstract
   public
   __construct()
public
   static
   getLastSocketErrno(
    mixed
     $socket
     = null
   ): int
public
   static
   getLastSocketError(
    mixed
     $socket
    = ?): string
public
   static
   getSocketFd(
    mixed
     $socket
   ): int
public
   static
   getSocketName(
    mixed
     $socket
   , 
    string
     &$address
   , 
    mixed
     &$port
    = ?): bool
public
   static
   setSocketOption(    
    mixed
     $socket
   ,    
    int
     $level
   ,    
    int
     $optname
   ,    
    mixed
     $optval
   ): bool
public
   static
   sslRandPoll(): void

   }
```

## Обумовлені константи

**`EventUtil::AF_INET`**

Сімейство IPv4 адрес

**`EventUtil::AF_INET6`**

Сімейство IPv6 адрес

**`EventUtil::AF_UNSPEC`**

Невизначена родина IP-адрес

**`EventUtil::SO_DEBUG`**

Опція сокету. Дозволяє налагодження сокету. Допустимо лише для процесів з можливістю `CAP_NET_ADMIN` або для користувача з ефективним ідентифікатором **`0`** . (Додано в event-1.6.0.)

**`EventUtil::SO_REUSEADDR`**

Опція сокету. Вказує, що правила, які використовуються при перевірці адрес, що задаються у виклику `bind(2)` дозволяють перевикористовувати локальні адреси. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_KEEPALIVE`**

Опція сокету. Дозволяє надсилати повідомлення keep-alive на сокетах, орієнтованих на з'єднання. Очікується цілий логічний прапор. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_DONTROUTE`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_LINGER`**

Опція сокету. Якщо дозволено, то дзвінки `close(2)` або `shutdown(2)` не буде завершено, доки всі повідомлення в черзі для сокету не будуть успішно надіслані, або поки не буде перевищено час очікування. Інакше дзвінок негайно завершується, а закриття виконується у фоновому режимі. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_BROADCAST`**

Опція сокету. Вказує, чи дозволено передачу широкомовних повідомлень. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_OOBINLINE`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_SNDBUF`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_RCVBUF`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_SNDLOWAT`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_RCVLOWAT`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_SNDTIMEO`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_RCVTIMEO`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_TYPE`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SO_ERROR`**

Опція сокету. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SOL_SOCKET`**

Опція сокету рівень. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SOL_TCP`**

Опція сокету рівень. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::SOL_UDP`**

Опція сокету рівень. Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::IPPROTO_IP`**

Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::IPPROTO_IPV6`**

Дивіться посібник з `socket(7)`. (Додано в event-1.6.0.)

**`EventUtil::LIBEVENT_VERSION_NUMBER`**

Номер версії libevent з якою компілювався модуль.

## Зміст

-   [EventUtil::construct](eventutil.construct.md) - Абстрактний конструктор
-   [EventUtil::getLastSocketErrno](eventutil.getlastsocketerrno.md) — Отримати номер останньої помилки сокету, що виникла.
-   [EventUtil::getLastSocketError](eventutil.getlastsocketerror.md) — Отримати останню помилку сокету, що виникла.
-   [EventUtil::getSocketFd](eventutil.getsocketfd.md) — Отримати цифровий файловий дескриптор сокету чи потоку
-   [EventUtil::getSocketName](eventutil.getsocketname.md) — Отримати поточну адресу, до якої прив'язаний сокет
-   [EventUtil::setSocketOption](eventutil.setsocketoption.md) - Встановити опції сокету
-   [EventUtil::sslRandPoll](eventutil.sslrandpoll.md) - Згенерувати ентропію за допомогою RANDpoll() із OpenSSL