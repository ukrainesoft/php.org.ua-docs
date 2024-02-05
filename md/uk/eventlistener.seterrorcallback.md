---
navigation:
  - eventlistener.setcallback.md: '« EventListener::setCallback'
  - class.eventsslcontext.md: EventSslContext »
  - index.md: PHP Manual
  - class.eventlistener.md: EventListener
title: 'EventListener::setErrorCallback'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# EventListener::setErrorCallback

(PECL event >= 1.2.6-beta)

EventListener::setErrorCallback — Встановлює callback-функцію помилки слухача подій

### Опис

```methodsynopsis
public
   EventListener::setErrorCallback(
    string
     $cb
   ): void
```

Встановлює callback-функцію помилки слухача подій

### Список параметрів

`cb`

Callback-функція помилки. Повинна відповідати наступному прототипу:

```methodsynopsis
callback(
       EventListener
        $listener
        = null
      , 
       mixed
        $data
        = null
      ): void
```

`listener`

Об'єкт [EventListener](class.eventlistener.md)

`data`

Ці дані, прикріплені до callback-функції.

### Значення, що повертаються

### Дивіться також

-   [EventListener::setCallback()](eventlistener.setcallback.md) \- Ціль setCallback
