Про callback-функції подієвого буфера

-   [« EventBufferEvent::writeBuffer](eventbufferevent.writebuffer.md)
    
-   [EventConfig »](class.eventconfig.md)
    
-   [PHP Manual](index.md)
    
-   [Event](book.event.md)
    
-   Про callback-функції подієвого буфера
    

# Про callback-функції подієвого буфера

Об'єкт класу [EventBufferEvent](class.eventbufferevent.md) представляє *буфер подій*. Асинхронна природа введення/виводу Libevent передбачає, що сокет (або якийсь інший файловий дескриптор) не завжди доступний. Модуль викликає відповідні callback-функції, коли ресурс готовий до читання або запису, або коли відбулася якась подія (наприклад, помилка, або кінець файлу тощо).

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

Пов'язаний об'єкт [EventBufferEvent](class.eventbufferevent.md)

`arg`

Дані користувача прив'язані до всіх callback-функцій через [EventBufferEvent::construct()](eventbufferevent.construct.md) або [EventBufferEvent::setCallbacks()](eventbufferevent.setcallbacks.md)

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

Пов'язаний об'єкт [EventBufferEvent](class.eventbufferevent.md)

`events`

Бітова маска подій: **`EventBufferEvent::READING`** **`EventBufferEvent::WRITING`** **`EventBufferEvent::EOL`** **`EventBufferEvent::ERROR`** і **`EventBufferEvent::TIMEOUT`** . Дивіться [Константи EventBufferEvent](class.eventbufferevent.html#eventbufferevent.constants)

`arg`

Дані користувача прив'язані до всіх callback-функцій через [EventBufferEvent::construct()](eventbufferevent.construct.md) або [EventBufferEvent::setCallbacks()](eventbufferevent.setcallbacks.md)