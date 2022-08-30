Встановлює callback-функцію помилки слухача подій

-   [« EventListener::setCallback](eventlistener.setcallback.md)
    
-   [EventSslContext »](class.eventsslcontext.md)
    
-   [PHP Manual](index.md)
    
-   [EventListener](class.eventlistener.md)
    
-   Встановлює callback-функцію помилки слухача подій
    

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

-   [EventListener::setCallback()](eventlistener.setcallback.md) - Ціль setCallback