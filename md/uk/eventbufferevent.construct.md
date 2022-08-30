Створює об'єкт EventBufferEvent

-   [« EventBufferEvent::connectHost](eventbufferevent.connecthost.html)
    
-   [EventBufferEvent::createPair »](eventbufferevent.createpair.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Створює об'єкт EventBufferEvent
    

# EventBufferEvent::construct

(PECL event >= 1.2.6-beta)

EventBufferEvent::construct — Створює об'єкт EventBufferEvent

### Опис

```methodsynopsis
public
   EventBufferEvent::__construct(    
    EventBase
     $base
   ,    
    mixed
     $socket
     = null
   ,    
    int
     $options
     = 0
   ,    
    callable
     $readcb
     = null
   ,    
    callable
     $writecb
     = null
   ,    
    callable
     $eventcb
     = null
   ,    
    mixed
     $arg
     = null
   )
```

Створює подію буфера для сокету, потоку чи файлового дескриптора. Передача **`null`** в `socket` означає, що сокет повинен бути створений пізніше, наприклад, за допомогою [EventBufferEvent::connect()](eventbufferevent.connect.html)

### Список параметрів

`base`

База події, яка має бути пов'язана з новою буферною подією.

`socket`

Може бути створений у вигляді потоку (не обов'язково за допомогою модуля `sockets`

`options`

Одна з [констант EventBufferEvent::OPT](class.eventbufferevent.html#eventbufferevent.constants) або **`0`**

`readcb`

Callback-функція читання. Зверніться до розділу [О callback-функциях событийного буфера](eventbufferevent.about.callbacks.html)

`writecb`

Callback-функція запису. Зверніться до розділу [О callback-функциях событийного буфера](eventbufferevent.about.callbacks.html)

`eventcb`

Callback – функція події зміни статусу. Зверніться до розділу [О callback-функциях событийного буфера](eventbufferevent.about.callbacks.html)

`arg`

Змінна, яка буде передана всім callback-функціям.

### Значення, що повертаються

Повертає ресурс події буфера, пов'язаний у разі потреби з ресурсом сокету.

### Дивіться також

-   [EventBufferEvent::sslFilter()](eventbufferevent.sslfilter.html) - Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера
-   [EventBufferEvent::sslSocket()](eventbufferevent.sslsocket.html) - Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет