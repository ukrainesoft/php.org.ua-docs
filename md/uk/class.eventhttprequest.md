---
navigation:
  - eventhttpconnection.settimeout.md: '« EventHttpConnection::setTimeout'
  - eventhttprequest.addheader.md: 'EventHttpRequest::addHeader »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventHttpRequest
---
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

-   [EventHttpRequest::addHeader](eventhttprequest.addheader.md) — Додає заголовок HTTP до заголовків запиту
-   [EventHttpRequest::cancel](eventhttprequest.cancel.md) — Скасує очікування HTTP-запиту
-   [EventHttpRequest::clearHeaders](eventhttprequest.clearheaders.md) — Видаляє всі вихідні заголовки зі списку заголовків запиту
-   [EventHttpRequest::closeConnection](eventhttprequest.closeconnection.md) — Закриває пов'язане з'єднання HTTP
-   [EventHttpRequest::construct](eventhttprequest.construct.md) - Конструктор об'єкта EventHttpRequest
-   [EventHttpRequest::findHeader](eventhttprequest.findheader.md) — Отримує значення заголовка
-   [EventHttpRequest::free](eventhttprequest.free.md) — Звільняє об'єкт та видаляє пов'язані події
-   [EventHttpRequest::getBufferEvent](eventhttprequest.getbufferevent.md) — Повертає об'єкт EventBufferEvent
-   [EventHttpRequest::getCommand](eventhttprequest.getcommand.md) - Повертає команду запиту (метод)
-   [EventHttpRequest::getConnection](eventhttprequest.getconnection.md) — Повертає об'єкт EventHttpConnection
-   [EventHttpRequest::getHost](eventhttprequest.gethost.md) - Повертає хост запиту
-   [EventHttpRequest::getInputBuffer](eventhttprequest.getinputbuffer.md) - Повертає вхідний буфер
-   [EventHttpRequest::getInputHeaders](eventhttprequest.getinputheaders.md) - Повертає асоціативний масив вхідних заголовків
-   [EventHttpRequest::getOutputBuffer](eventhttprequest.getoutputbuffer.md) — Повертає вихідний буфер запиту
-   [EventHttpRequest::getOutputHeaders](eventhttprequest.getoutputheaders.md) — Повертає асоціативний масив вихідних заголовків
-   [EventHttpRequest::getResponseCode](eventhttprequest.getresponsecode.md) - Повертає код відповіді
-   [EventHttpRequest::getUri](eventhttprequest.geturi.md) — Повертає запит URI
-   [EventHttpRequest::removeHeader](eventhttprequest.removeheader.md) — Видаляє заголовок HTTP із заголовків запиту
-   [EventHttpRequest::sendError](eventhttprequest.senderror.md) — Надсилає HTML-повідомлення про помилку клієнту
-   [EventHttpRequest::sendReply](eventhttprequest.sendreply.md) — Відправляє HTML-відповідь клієнту
-   [EventHttpRequest::sendReplyChunk](eventhttprequest.sendreplychunk.md) — Відправляє блок даних як частину поточної фрагментованої відповіді
-   [EventHttpRequest::sendReplyEnd](eventhttprequest.sendreplyend.md) — Заповнює фрагментарну відповідь, звільняючи запит належним чином
-   [EventHttpRequest::sendReplyStart](eventhttprequest.sendreplystart.md) — Ініціює фрагментарну відповідь
