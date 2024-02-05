---
navigation:
  - eventhttp.settimeout.md: '« EventHttp::setTimeout'
  - eventhttpconnection.construct.md: 'EventHttpConnection::\_\_construct »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventHttpConnection
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

-   [EventHttpConnection::\_\_construct](eventhttpconnection.construct.md)— Створює об'єкт EventHttpConnection
-   [EventHttpConnection::getBase](eventhttpconnection.getbase.md)— Повертає базу подій, пов'язану із з'єднанням
-   [EventHttpConnection::getPeer](eventhttpconnection.getpeer.md)— Отримує віддалену адресу та порт, пов'язаний зі з'єднанням
-   [EventHttpConnection::makeRequest](eventhttpconnection.makerequest.md)— Робить HTTP-запит із зазначеного з'єднання
-   [EventHttpConnection::setCloseCallback](eventhttpconnection.setclosecallback.md) \- Встановлює callback-функцію при закритті з'єднання
-   [EventHttpConnection::setLocalAddress](eventhttpconnection.setlocaladdress.md)— Встановлює IP-адресу, з якої відбуваються HTTP-з'єднання.
-   [EventHttpConnection::setLocalPort](eventhttpconnection.setlocalport.md)— Встановлює локальний порт, з якого виробляються з'єднання.
-   [EventHttpConnection::setMaxBodySize](eventhttpconnection.setmaxbodysize.md)— Встановлює максимальний розмір тіла для підключення
-   [EventHttpConnection::setMaxHeadersSize](eventhttpconnection.setmaxheaderssize.md) \- Встановлює максимальний розмір заголовка
-   [EventHttpConnection::setRetries](eventhttpconnection.setretries.md)— Встановлює максимальну кількість повторів для з'єднання
-   [EventHttpConnection::setTimeout](eventhttpconnection.settimeout.md)— Встановлює час очікування на з'єднання
