Клас EventHttpRequest

-   [« EventHttpConnection::setTimeout](eventhttpconnection.settimeout.html)
    
-   [EventHttpRequest::addHeader »](eventhttprequest.addheader.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventHttpRequest
    

# Клас EventHttpRequest

(PECL event >= 1.4.0-beta)

## Вступ

Надає HTTP-запит.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EventHttpRequest
     
     {
    
    /* Константы */
    
     const
     int
      CMD_GET = 1;

    const
     int
      CMD_POST = 2;

    const
     int
      CMD_HEAD = 4;

    const
     int
      CMD_PUT = 8;

    const
     int
      CMD_DELETE = 16;

    const
     int
      CMD_OPTIONS = 32;

    const
     int
      CMD_TRACE = 64;

    const
     int
      CMD_CONNECT = 128;

    const
     int
      CMD_PATCH = 256;

    const
     int
      INPUT_HEADER = 1;

    const
     int
      OUTPUT_HEADER = 2;

    /* Методы */
    
   public
   addHeader(
    string
     $key
   , 
    string
     $value
   , 
    int
     $type
   ): bool
public
   cancel(): void
public
   clearHeaders(): void
public
   closeConnection(): void
public
   __construct(
    callable
     $callback
   , 
    mixed
     $data
     = null
   )
public
   findHeader(
    string
     $key
   , 
    string
     $type
   ): void
public
   free(): void
public
   closeConnection(): EventBufferEvent
public
   getCommand(): void
public
   closeConnection(): EventHttpConnection
public
   getHost(): string
public
   getInputBuffer(): EventBuffer
public
   getInputHeaders(): array
public
   getOutputBuffer(): EventBuffer
public
   getOutputHeaders(): void
public
   getResponseCode(): int
public
   getUri(): string
public
   removeHeader(
    string
     $key
   , 
    string
     $type
   ): void
public
   sendError(
    int
     $error
   , 
    string
     $reason
     = null
   ): void
public
   sendReply(
    int
     $code
   , 
    string
     $reason
   , 
    EventBuffer
     $buf
    = ?): void
public
   sendReplyChunk(
    EventBuffer
     $buf
   ): void
public
   sendReplyEnd(): void
public
   sendReplyStart(
    int
     $code
   , 
    string
     $reason
   ): void

   }
```

## Обумовлені константи

**`EventHttpRequest::CMD_GET`**

Метод GET (команда)

**`EventHttpRequest::CMD_POST`**

Метод POST (команда)

**`EventHttpRequest::CMD_HEAD`**

Метод HEAD (команда)

**`EventHttpRequest::CMD_PUT`**

Метод PUT (команда)

**`EventHttpRequest::CMD_DELETE`**

Метод DELETE (команда)

**`EventHttpRequest::CMD_OPTIONS`**

Метод OPTIONS (команда)

**`EventHttpRequest::CMD_TRACE`**

Метод TRACE (команда)

**`EventHttpRequest::CMD_CONNECT`**

Метод CONNECT (команда)

**`EventHttpRequest::CMD_PATCH`**

Метод PATCH (команда)

**`EventHttpRequest::INPUT_HEADER`**

Тип вхідного заголовка запиту.

**`EventHttpRequest::OUTPUT_HEADER`**

Тип вихідного заголовка запиту.

## Зміст

-   [EventHttpRequest::addHeader](eventhttprequest.addheader.html) — Додає заголовок HTTP до заголовків запиту
-   [EventHttpRequest::cancel](eventhttprequest.cancel.html) — Скасує очікування HTTP-запиту
-   [EventHttpRequest::clearHeaders](eventhttprequest.clearheaders.html) — Видаляє всі вихідні заголовки зі списку заголовків запиту
-   [EventHttpRequest::closeConnection](eventhttprequest.closeconnection.html) — Закриває пов'язане з'єднання HTTP
-   [EventHttpRequest::\_\_construct](eventhttprequest.construct.html) - Конструктор об'єкта EventHttpRequest
-   [EventHttpRequest::findHeader](eventhttprequest.findheader.html) — Отримує значення заголовка
-   [EventHttpRequest::free](eventhttprequest.free.html) — Звільняє об'єкт та видаляє пов'язані події
-   [EventHttpRequest::getBufferEvent](eventhttprequest.getbufferevent.html) — Повертає об'єкт EventBufferEvent
-   [EventHttpRequest::getCommand](eventhttprequest.getcommand.html) - Повертає команду запиту (метод)
-   [EventHttpRequest::getConnection](eventhttprequest.getconnection.html) — Повертає об'єкт EventHttpConnection
-   [EventHttpRequest::getHost](eventhttprequest.gethost.html) - Повертає хост запиту
-   [EventHttpRequest::getInputBuffer](eventhttprequest.getinputbuffer.html) - Повертає вхідний буфер
-   [EventHttpRequest::getInputHeaders](eventhttprequest.getinputheaders.html) - Повертає асоціативний масив вхідних заголовків
-   [EventHttpRequest::getOutputBuffer](eventhttprequest.getoutputbuffer.html) — Повертає вихідний буфер запиту
-   [EventHttpRequest::getOutputHeaders](eventhttprequest.getoutputheaders.html) — Повертає асоціативний масив вихідних заголовків
-   [EventHttpRequest::getResponseCode](eventhttprequest.getresponsecode.html) - Повертає код відповіді
-   [EventHttpRequest::getUri](eventhttprequest.geturi.html) — Повертає запит URI
-   [EventHttpRequest::removeHeader](eventhttprequest.removeheader.html) — Видаляє заголовок HTTP із заголовків запиту
-   [EventHttpRequest::sendError](eventhttprequest.senderror.html) — Надсилає HTML-повідомлення про помилку клієнту
-   [EventHttpRequest::sendReply](eventhttprequest.sendreply.html) — Відправляє HTML-відповідь клієнту
-   [EventHttpRequest::sendReplyChunk](eventhttprequest.sendreplychunk.html) — Відправляє блок даних як частину поточної фрагментованої відповіді
-   [EventHttpRequest::sendReplyEnd](eventhttprequest.sendreplyend.html) — Заповнює фрагментарну відповідь, звільняючи запит належним чином
-   [EventHttpRequest::sendReplyStart](eventhttprequest.sendreplystart.html) — Ініціює фрагментарну відповідь