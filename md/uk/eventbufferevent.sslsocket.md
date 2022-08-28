Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет

-   [« EventBufferEvent::sslRenegotiate](eventbufferevent.sslrenegotiate.html)
    
-   [EventBufferEvent::write »](eventbufferevent.write.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет
    

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

Сокет для використання для SSL. Може бути ресурсом потоку або сокету, числовим дескриптором файлу або **`null`**. Якщо `socket` дорівнює **`null`**, передбачається, що файловий дескриптор для сокету буде призначено пізніше, наприклад, за допомогою методу [EventBufferEvent::connectHost()](eventbufferevent.connecthost.html)

`ctx`

Об'єкт класу [EventSslContext](class.eventsslcontext.html)

`state`

Поточний стан з'єднання SSL: **`EventBufferEvent::SSL_OPEN`** **`EventBufferEvent::SSL_ACCEPTING`** або **`EventBufferEvent::SSL_CONNECTING`**

`options`

Настройки буферної події.

### Значення, що повертаються

Повертає об'єкт [EventBufferEvent](class.eventbufferevent.html)

### Дивіться також

-   [EventBufferEvent::sslFilter()](eventbufferevent.sslfilter.html) - Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера