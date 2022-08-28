Про callback-функції подієвого буфера

-   [« EventBufferEvent::writeBuffer](eventbufferevent.writebuffer.html)
    
-   [EventConfig »](class.eventconfig.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Про callback-функції подієвого буфера
    

# Про callback-функції подієвого буфера

Об'єкт класу [EventBufferEvent](class.eventbufferevent.html) представляє *буфер подій*. Асинхронна природа введення/виводу Libevent передбачає, що сокет (або якийсь інший файловий дескриптор) не завжди доступний. Модуль викликає відповідні callback-функції, коли ресурс готовий до читання або запису, або коли відбулася якась подія (наприклад, помилка, або кінець файлу тощо).

Callback-функції читання та запису повинні відповідати наступному прототипу:

```methodsynopsis
callback(
   EventBufferEvent
     $bev
     = null
  , 
   mixed
     $arg
     = null
  ): void
```

`bev`

Пов'язаний об'єкт [EventBufferEvent](class.eventbufferevent.html)

`arg`

Дані користувача прив'язані до всіх callback-функцій через [EventBufferEvent::\_\_construct()](eventbufferevent.construct.html) або [EventBufferEvent::setCallbacks()](eventbufferevent.setcallbacks.html)

Callback-функції подій повинні відповідати наступному прототипу:

```methodsynopsis
callback(
   EventBufferEvent
     $bev
     = null
  , 
   int
     $events
     = 0
  , 
   mixed
     $arg
     = null
  ): void
```

`bev`

Пов'язаний об'єкт [EventBufferEvent](class.eventbufferevent.html)

`events`

Бітова маска подій: **`EventBufferEvent::READING`** **`EventBufferEvent::WRITING`** **`EventBufferEvent::EOL`** **`EventBufferEvent::ERROR`** і **`EventBufferEvent::TIMEOUT`** . Дивіться [Константы EventBufferEvent](class.eventbufferevent.html#eventbufferevent.constants)

`arg`

Дані користувача прив'язані до всіх callback-функцій через [EventBufferEvent::\_\_construct()](eventbufferevent.construct.html) або [EventBufferEvent::setCallbacks()](eventbufferevent.setcallbacks.html)