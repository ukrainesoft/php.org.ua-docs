Додає дані до кінця буфера подій

-   [« EventBuffer](class.eventbuffer.md)
    
-   [EventBuffer::addBuffer »](eventbuffer.addbuffer.md)
    
-   [PHP Manual](index.md)
    
-   [EventBuffer](class.eventbuffer.md)
    
-   Додає дані до кінця буфера подій
    

# EventBuffer::add

(PECL event >= 1.2.6-beta)

EventBuffer::add — Додає дані до кінця буфера подій

### Опис

```methodsynopsis
public
   EventBuffer::add(
    string
     $data
   ): bool
```

Додає дані до кінця буфера подій

### Список параметрів

`data`

Рядок, який буде додано в кінець буфера.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.

### Дивіться також

-   [EventBuffer::addBuffer()](eventbuffer.addbuffer.md) - Переміщує всі дані з буфера екземпляру EventBuffer