Обрізає частину даних буфера

-   [« EventBuffer::searchEol](eventbuffer.searcheol.md)
    
-   [EventBuffer::unfreeze »](eventbuffer.unfreeze.md)
    
-   [PHP Manual](index.md)
    
-   [EventBuffer](class.eventbuffer.md)
    
-   Обрізає частину даних буфера
    

# EventBuffer::substr

(PECL event >= 1.6.0)

EventBuffer::substr — Обрізає частину даних буфера

### Опис

```methodsynopsis
public
   EventBuffer::substr(
    int
     $start
   , 
    int
     $length
    = ?): string
```

Обрізає до `length` байтів даних буфера, починаючи з позиції `start`

### Список параметрів

`start`

Початкова позиція даних, що підлягають обрізанню.

`length`

Максимальна кількість байтів для обрізання.

### Значення, що повертаються

Повертає дані, вираховані у вигляді рядка (string) у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::read()](eventbuffer.read.md) - Читає дані з evbuffer та виснажує прочитані байти