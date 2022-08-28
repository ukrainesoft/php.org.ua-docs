Повторно включає дзвінки, які змінюють буфер подій

-   [« EventBuffer::substr](eventbuffer.substr.html)
    
-   [EventBuffer::unlock »](eventbuffer.unlock.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Повторно включає дзвінки, які змінюють буфер подій
    

# EventBuffer::unfreeze

(PECL event >= 1.2.6-beta)

EventBuffer::unfreeze — Повторно включає дзвінки, які змінюють буфер подій

### Опис

```methodsynopsis
public
   EventBuffer::unfreeze(
    bool
     $at_front
   ): bool
```

Повторно включає дзвінки, які змінюють буфер подій.

### Список параметрів

`at_front`

Визначає увімкнути події на початку або в кінці буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::freeze()](eventbuffer.freeze.html) - Запобігає викликам, які змінюють буфер подій у разі успішного виконання