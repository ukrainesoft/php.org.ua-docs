---
navigation:
  - eventbufferevent.connecthost.md: '« EventBufferEvent::connectHost'
  - eventbufferevent.createpair.md: 'EventBufferEvent::createPair »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::construct'
---
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

Створює подію буфера для сокету, потоку чи файлового дескриптора. Передача **`null`** в `socket` означає, що сокет повинен бути створений пізніше, наприклад, за допомогою [EventBufferEvent::connect()](eventbufferevent.connect.md)

### Список параметрів

`base`

База події, яка має бути пов'язана з новою буферною подією.

`socket`

Може бути створений у вигляді потоку (не обов'язково за допомогою модуля `sockets`

`options`

Одна з [констант EventBufferEvent::OPT](class.eventbufferevent.md#eventbufferevent.constants) або **`0`**

`readcb`

Callback-функція читання. Зверніться до розділу [Про callback-функції подієвого буфера](eventbufferevent.about.callbacks.md)

`writecb`

Callback-функція запису. Зверніться до розділу [Про callback-функції подієвого буфера](eventbufferevent.about.callbacks.md)

`eventcb`

Callback – функція події зміни статусу. Зверніться до розділу [Про callback-функції подієвого буфера](eventbufferevent.about.callbacks.md)

`arg`

Змінна, яка буде передана всім callback-функціям.

### Значення, що повертаються

Повертає ресурс події буфера, пов'язаний у разі потреби з ресурсом сокету.

### Дивіться також

-   [EventBufferEvent::sslFilter()](eventbufferevent.sslfilter.md) - Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера
-   [EventBufferEvent::sslSocket()](eventbufferevent.sslsocket.md) - Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет
