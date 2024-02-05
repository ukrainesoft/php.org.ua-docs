---
navigation:
  - eventbufferevent.connecthost.md: '« EventBufferEvent::connectHost'
  - eventbufferevent.createpair.md: 'EventBufferEvent::createPair »'
  - index.md: PHP Manual
  - class.eventbufferevent.md: EventBufferEvent
title: 'EventBufferEvent::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventBufferEvent::\_\_construct

(PECL event >= 1.2.6-beta)

EventBufferEvent::\_\_construct — Створює об'єкт EventBufferEvent

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

Створює подію буфера для сокету, потоку чи файлового дескриптора. Передача \*\*`null`\*\*в`socket` означає, що сокет повинен бути створений пізніше, наприклад, за допомогою [EventBufferEvent::connect()](eventbufferevent.connect.md)

### Список параметрів

`base`

База події, яка має бути пов'язана з новою буферною подією.

`socket`

Дозволено створювати у вигляді потоку (не обов'язково засобами модуля `sockets`

`options`

Константа семейства[EventBufferEvent::OPT\_\*](class.eventbufferevent.md#eventbufferevent.constants)или

`readcb`

Callback-функція події читання. Докладніше розказано у розділі « [Про callback-функції подієвого буфера](eventbufferevent.about.callbacks.md) ».

`writecb`

Callback – функція події запису. Докладніше розказано у розділі « [Про callback-функції подієвого буфера](eventbufferevent.about.callbacks.md) ».

`eventcb`

Callback – функція події зміни статусу. Докладніше розказано у розділі « [Про callback-функції подієвого буфера](eventbufferevent.about.callbacks.md) ».

`arg`

Змінна, яка буде передана кожній callback-функції.

### Дивіться також

-   [EventBufferEvent::sslFilter()](eventbufferevent.sslfilter.md) \- Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера
-   [EventBufferEvent::sslSocket()](eventbufferevent.sslsocket.md) \- Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет
