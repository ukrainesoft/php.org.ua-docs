Опис

-   [« EventBuffer::drain](eventbuffer.drain.html)
    
-   [EventBuffer::expand »](eventbuffer.expand.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Опис
    

# EventBuffer::enableLocking

(PECL event >= 1.2.6-beta)

EventBuffer::enableLocking -

### Опис

```methodsynopsis
public
   EventBuffer::enableLocking(): void
```

Включає блокування для [EventBuffer](class.eventbuffer.html)щоб він міг безпечно використовуватися кількома потоками одночасно. Коли блокування увімкнено, воно буде утримуватися при виклику callback-функцій. Це може призвести до глухого кута, якщо ви не будете обережні. Плануйте відповідно!

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [» Evbuffers та Thread-безпека](http://www.wangafu.net/~nickm/libevent-book/Ref7_evbuffer.html#_evbuffers_and_thread_safety)