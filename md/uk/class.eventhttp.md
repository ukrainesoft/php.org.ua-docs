---
navigation:
  - eventdnsbase.setsearchndots.md: '« EventDnsBase::setSearchNdots'
  - eventhttp.accept.md: 'EventHttp::accept »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventHttp
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Клас EventHttp

(PECL event >= 1.4.0-beta)

## Вступ

Надає сервер HTTP.

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventHttp
     
     {
    
    /* Методы */
    
   public
   accept(
    mixed
     $socket
   ): bool
public
   addServerAlias(
    string
     $alias
   ): bool
public
   bind(
    string
     $address
   , 
    int
     $port
   ): void
public
   __construct(
    EventBase
     $base
   , 
    EventSslContext
     $ctx
     = null
   )
public
   removeServerAlias(
    string
     $alias
   ): bool
public
   setAllowedMethods(
    int
     $methods
   ): void
public
   setCallback(
    string
     $path
   , 
    string
     $cb
   , 
    string
     $arg
    = ?): void
public
   setDefaultCallback(
    string
     $cb
   , 
    string
     $arg
    = ?): void
public
   setMaxBodySize(
    int
     $value
   ): void
public
   setMaxHeadersSize(
    int
     $value
   ): void
public
   setTimeout(
    int
     $value
   ): void

   }
```

## Зміст

-   [EventHttp::accept](eventhttp.accept.md)— Примушує HTTP-сервер приймати з'єднання із зазначеним потоком сокету чи ресурсом
-   [EventHttp::addServerAlias](eventhttp.addserveralias.md)— Додає псевдонім сервера до об'єкта HTTP-сервера
-   [EventHttp::bind](eventhttp.bind.md)— Прив'язує HTTP-сервер до вказаної адреси та порту
-   [EventHttp::\_\_construct](eventhttp.construct.md)— Створює об'єкт EventHttp (сервер HTTP)
-   [EventHttp::removeServerAlias](eventhttp.removeserveralias.md)— Видаляє псевдонім сервера
-   [EventHttp::setAllowedMethods](eventhttp.setallowedmethods.md)— Встановлює, які методи HTTP підтримуються у запитах, прийнятих цим сервером та переданих callback-функції користувача
-   [EventHttp::setCallback](eventhttp.setcallback.md)— Встановлює callback-функцію для вказаного URI
-   [EventHttp::setDefaultCallback](eventhttp.setdefaultcallback.md) \- Встановлює callback-функцію за замовчуванням для обробки запитів, які не перехоплюються конкретними callback-функціями
-   [EventHttp::setMaxBodySize](eventhttp.setmaxbodysize.md) \- Встановлює максимальний розмір тіла запиту
-   [EventHttp::setMaxHeadersSize](eventhttp.setmaxheaderssize.md)— Встановлює максимальний розмір заголовка HTTP
-   [EventHttp::setTimeout](eventhttp.settimeout.md)— Встановлює час очікування для запиту HTTP
