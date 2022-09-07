---
navigation:
  - eventbufferevent.sslrenegotiate.md: '« EventBufferEvent::sslRenegotiate'
  - eventbufferevent.write.md: 'EventBufferEvent::write »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::sslSocket'
---
# EventBufferEvent::sslSocket

(PECL event >= 1.2.6-beta)

EventBufferEvent::sslSocket — Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет

### Опис

```methodsynopsis
public
   static
   EventBufferEvent::sslSocket(    
    EventBase
     $base
   ,    
    mixed
     $socket
   ,    
    EventSslContext
     $ctx
   ,    
    int
     $state
   ,    
    int
     $options
    = ?): EventBufferEvent
```

Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет.

### Список параметрів

`base`

Пов'язана основа подій.

`socket`

Сокет для використання для SSL. Може бути ресурсом потоку або сокету, числовим дескриптором файлу або **`null`**. Якщо `socket` дорівнює **`null`**, передбачається, що файловий дескриптор для сокету буде призначено пізніше, наприклад, за допомогою методу [EventBufferEvent::connectHost()](eventbufferevent.connecthost.md)

`ctx`

Об'єкт класу [EventSslContext](class.eventsslcontext.md)

`state`

Поточний стан з'єднання SSL: **`EventBufferEvent::SSL_OPEN`** **`EventBufferEvent::SSL_ACCEPTING`** або **`EventBufferEvent::SSL_CONNECTING`**

`options`

Настройки буферної події.

### Значення, що повертаються

Повертає об'єкт [EventBufferEvent](class.eventbufferevent.md)

### Дивіться також

-   [EventBufferEvent::sslFilter()](eventbufferevent.sslfilter.md) - Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера
