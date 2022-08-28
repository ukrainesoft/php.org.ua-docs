Отримує блокування буфера

-   [« EventBuffer::freeze](eventbuffer.freeze.html)
    
-   [EventBuffer::prepend »](eventbuffer.prepend.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Отримує блокування буфера
    

# EventBuffer::lock

(PECL event >= 1.2.6-beta)

EventBuffer::lock — Отримує блокування буфера

### Опис

```methodsynopsis
public
   EventBuffer::lock(): void
```

Отримує блокування буфера. Може використовуватися в парі з [EventBuffer::unlock()](eventbuffer.unlock.html)щоб зробити набір операцій атомарним, тобто потокобезпечним. Зверніть увагу, що немає необхідності блокувати буфери для *окремих* операцій. Коли блокування увімкнено (дивіться [EventBuffer::enableLocking()](eventbuffer.enablelocking.html)), окремі операції над буферами подій є атомарними.

### Список параметрів

Ця функція не має параметрів.

### Значення, що повертаються

Функція не повертає значення після виконання.

### Дивіться також

-   [EventBuffer::unlock()](eventbuffer.unlock.html) - Знімає блокування, встановлене EventBuffer::lock