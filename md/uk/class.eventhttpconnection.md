Клас EventHttpConnection

-   [« EventHttp::setTimeout](eventhttp.settimeout.html)
    
-   [EventHttpConnection::\_\_construct »](eventhttpconnection.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventHttpConnection
    

# Клас EventHttpConnection

(PECL event >= 1.4.0-beta)

## Вступ

Надає HTTP-з'єднання.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EventHttpConnection
     
     {
    
    /* Методы */
    
   public
   __construct(    
    EventBase
     $base
   ,    
    EventDnsBase
     $dns_base
   ,    
    string
     $address
   ,    
    int
     $port
   ,    
    EventSslContext
     $ctx
     = null
   )
public
   getBase(): EventBase
public
   getPeer(
    string
     &$address
   , 
    int
     &$port
   ): void
public
   makeRequest(
    EventHttpRequest
     $req
   , 
    int
     $type
   , 
    string
     $uri
   ): bool
public
   setCloseCallback(
    callable
     $callback
   , 
    mixed
     $data
    = ?): void
public
   setLocalAddress(
    string
     $address
   ): void
public
   setLocalPort(
    int
     $port
   ): void
public
   setMaxBodySize(
    string
     $max_size
   ): void
public
   setMaxHeadersSize(
    string
     $max_size
   ): void
public
   setRetries(
    int
     $retries
   ): void
public
   setTimeout(
    int
     $timeout
   ): void

   }
```

## Зміст

-   [EventHttpConnection::\_\_construct](eventhttpconnection.construct.html) - Конструктор об'єкта EventHttpConnection
-   [EventHttpConnection::getBase](eventhttpconnection.getbase.html) — Повертає базу подій, пов'язану із з'єднанням
-   [EventHttpConnection::getPeer](eventhttpconnection.getpeer.html) — Отримує віддалену адресу та порт, пов'язаний зі з'єднанням
-   [EventHttpConnection::makeRequest](eventhttpconnection.makerequest.html) — Робить HTTP-запит із зазначеного з'єднання
-   [EventHttpConnection::setCloseCallback](eventhttpconnection.setclosecallback.html) - Встановлює callback-функцію при закритті з'єднання
-   [EventHttpConnection::setLocalAddress](eventhttpconnection.setlocaladdress.html) — Встановлює IP-адресу, з якої відбуваються HTTP-з'єднання.
-   [EventHttpConnection::setLocalPort](eventhttpconnection.setlocalport.html) — Встановлює локальний порт, з якого виробляються з'єднання.
-   [EventHttpConnection::setMaxBodySize](eventhttpconnection.setmaxbodysize.html) — Встановлює максимальний розмір тіла для підключення
-   [EventHttpConnection::setMaxHeadersSize](eventhttpconnection.setmaxheaderssize.html) - Встановлює максимальний розмір заголовка
-   [EventHttpConnection::setRetries](eventhttpconnection.setretries.html) — Встановлює максимальну кількість повторів для з'єднання
-   [EventHttpConnection::setTimeout](eventhttpconnection.settimeout.html) — Встановлює час очікування на з'єднання