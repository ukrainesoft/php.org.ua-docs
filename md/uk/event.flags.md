Прапори подій

-   [« Примеры](event.examples.html)
    
-   [Про постійні (persistent) події »](event.persistence.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Прапори подій
    

# Прапори подій

Прапор **`Event::READ`** вказує подію, яка стає активною, коли наданий файл (зазвичай потоковий ресурс чи сокет) готовий до читання.

Прапор **`Event::WRITE`** вказує подію, яка стає активною, коли наданий файл (зазвичай потоковий ресурс чи сокет) готовий до запису.

Прапор **`Event::SIGNAL`** використовується реалізації відстеження системних сигналів. Дивіться "Створення подій для сигналів" нижче.

Прапор **`Event::TIMEOUT`** означає, що активувалася подія після закінчення очікування (timeout). Прапор **`Event::TIMEOUT`** ігнорується при створенні події: її можна встановити за *додаванні*. Він задається в аргументі `$what` callback-функції, якщо сталася подія цього.

Також почитайте [» Fast portable non-blocking network programming with Libevent, Working with events, Event flags](http://www.wangafu.net/~nickm/libevent-book/Ref4_event.html#_the_event_flags)