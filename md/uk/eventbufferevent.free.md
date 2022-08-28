Звільняє подію буфера

-   [« EventBufferEvent::enable](eventbufferevent.enable.html)
    
-   [EventBufferEvent::getDnsErrorString »](eventbufferevent.getdnserrorstring.html)
    
-   [PHP Manual](index.html)
    
-   [EventBufferEvent](class.eventbufferevent.html)
    
-   Звільняє подію буфера
    

# EventBufferEvent::free

(PECL event >= 1.2.6-beta)

EventBufferEvent::free — Звільняє подію буфера

### Опис

```methodsynopsis
public
   EventBufferEvent::free(): void
```

Визволяє ресурси, виділені буферною подією.

Зазвичай немає необхідності викликати цей метод, оскільки це робиться у внутрішніх деструкторах об'єкта. Однак іноді скрипти виконуються довго і створюють безліч екземплярів, а іноді інтенсивно використовують пам'ять, тому необхідно якнайшвидше звільнити ресурси. У таких випадках **EventBufferEvent::free()** може використовуватися для захисту скрипту від досягнення `memory_limit`

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.