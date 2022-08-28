Записує дані на початок буфера

-   [« EventBuffer::lock](eventbuffer.lock.html)
    
-   [EventBuffer::prependBuffer »](eventbuffer.prependbuffer.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Записує дані на початок буфера
    

# EventBuffer::prepend

(PECL event >= 1.2.6-beta)

EventBuffer::prepend — Записує дані на початок буфера

### Опис

```methodsynopsis
public
   EventBuffer::prepend(
    string
     $data
   ): bool
```

Записує дані на початок буфера.

### Список параметрів

`data`

Рядок, який буде додано на початок буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::prependBuffer()](eventbuffer.prependbuffer.html) - Переміщує всі дані з вихідного буфера на початок поточного буфера
-   [EventBuffer::add()](eventbuffer.add.html) - Додає дані до кінця буфера подій
-   [EventBuffer::addBuffer()](eventbuffer.addbuffer.html) - Переміщує всі дані з буфера екземпляру EventBuffer