---
navigation:
  - eventbufferevent.writebuffer.md: '« EventBufferEvent::writeBuffer'
  - class.eventconfig.md: EventConfig »
  - index.md: PHP Manual
  - book.event.md: Event
title: Про callback-функції подієвого буфера
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Про callback-функції подієвого буфера

Об'єкт класу [EventBufferEvent](class.eventbufferevent.md)представляет*буфер подій*. Асинхронна природа введення/виводу Libevent передбачає, що сокет (або якийсь інший файловий дескриптор) не завжди доступний. Модуль викликає відповідні callback-функції, коли ресурс готовий до читання або запису, або коли відбулася якась подія (наприклад, помилка, або кінець файлу тощо).

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

Дані користувача прив'язані до всіх callback-функцій через [EventBufferEvent::\_\_construct()](eventbufferevent.construct.md) або [EventBufferEvent::setCallbacks()](eventbufferevent.setcallbacks.md)

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

Бітова маска подій: **`EventBufferEvent::READING`** **`EventBufferEvent::WRITING`** **`EventBufferEvent::EOL`** **`EventBufferEvent::ERROR`**и**`EventBufferEvent::TIMEOUT`**. Смотрите[Константи EventBufferEvent](class.eventbufferevent.md#eventbufferevent.constants)

`arg`

Дані користувача прив'язані до всіх callback-функцій через [EventBufferEvent::\_\_construct()](eventbufferevent.construct.md) або [EventBufferEvent::setCallbacks()](eventbufferevent.setcallbacks.md)
