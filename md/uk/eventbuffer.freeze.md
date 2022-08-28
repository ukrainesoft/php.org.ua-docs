Запобігає викликам, які змінюють буфер подій у разі успішного виконання

-   [« EventBuffer::expand](eventbuffer.expand.html)
    
-   [EventBuffer::lock »](eventbuffer.lock.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Запобігає викликам, які змінюють буфер подій у разі успішного виконання
    

# EventBuffer::freeze

(PECL event >= 1.2.6-beta)

EventBuffer::freeze — Запобігає викликам, які змінюють буфер подій у разі успішного виконання

### Опис

```methodsynopsis
public
   EventBuffer::freeze(
    bool
     $at_front
   ): bool
```

Запобігає викликам, які змінюють буфер подій у разі успішного виконання

### Список параметрів

`at_front`

Чи вимкнути зміни на початку або в кінці буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::unfreeze()](eventbuffer.unfreeze.html) - Повторно включає дзвінки, які змінюють буфер подій