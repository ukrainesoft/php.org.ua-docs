Клас EventHttp

-   [« EventDnsBase::setSearchNdots](eventdnsbase.setsearchndots.html)
    
-   [EventHttp::accept »](eventhttp.accept.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventHttp
    

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

-   [EventHttp::accept](eventhttp.accept.html) — Примушує HTTP-сервер приймати з'єднання із зазначеним потоком сокету чи ресурсом
-   [EventHttp::addServerAlias](eventhttp.addserveralias.html) — Додає псевдонім сервера до об'єкта HTTP-сервера
-   [EventHttp::bind](eventhttp.bind.html) — Прив'язує HTTP-сервер до вказаної адреси та порту
-   [EventHttp::\_\_construct](eventhttp.construct.html) — Створює об'єкт EventHttp (сервер HTTP)
-   [EventHttp::removeServerAlias](eventhttp.removeserveralias.html) — Видаляє псевдонім сервера
-   [EventHttp::setAllowedMethods](eventhttp.setallowedmethods.html) — Встановлює, які методи HTTP підтримуються у запитах, прийнятих цим сервером та переданих callback-функції користувача
-   [EventHttp::setCallback](eventhttp.setcallback.html) — Встановлює callback-функцію для вказаного URI
-   [EventHttp::setDefaultCallback](eventhttp.setdefaultcallback.html) — Встановлює callback-функцію за промовчанням для обробки запитів, які не перехоплюються конкретними callback-функціями
-   [EventHttp::setMaxBodySize](eventhttp.setmaxbodysize.html) - Встановлює максимальний розмір тіла запиту
-   [EventHttp::setMaxHeadersSize](eventhttp.setmaxheaderssize.html) — Встановлює максимальний розмір заголовка HTTP
-   [EventHttp::setTimeout](eventhttp.settimeout.html) — Встановлює час очікування для запиту HTTP