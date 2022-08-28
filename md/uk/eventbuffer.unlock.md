Знімає блокування, встановлене EventBuffer::lock

-   [« EventBuffer::unfreeze](eventbuffer.unfreeze.html)
    
-   [EventBuffer::write »](eventbuffer.write.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Знімає блокування, встановлене EventBuffer::lock
    

# EventBuffer::unlock

(PECL event >= 1.2.6-beta)

EventBuffer::unlock — Знімає блокування, встановлене EventBuffer::lock

### Опис

```methodsynopsis
public
   EventBuffer::unlock(): bool
```

Знімає блокування, встановлене [EventBuffer::lock()](eventbuffer.lock.html)

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::lock()](eventbuffer.lock.html) - Отримує блокування буфера