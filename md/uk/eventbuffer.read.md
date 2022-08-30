Читає дані з evbuffer та виснажує прочитані байти

-   [« EventBuffer::pullup](eventbuffer.pullup.md)
    
-   [EventBuffer::readFrom »](eventbuffer.readfrom.md)
    
-   [PHP Manual](index.md)
    
-   [EventBuffer](class.eventbuffer.md)
    
-   Читає дані з evbuffer та виснажує прочитані байти
    

# EventBuffer::read

(PECL event >= 1.6.0)

EventBuffer::read — Читає дані з evbuffer і виснажує прочитані байти

### Опис

```methodsynopsis
public
   EventBuffer::read(
    int
     $max_bytes
   ): string
```

Прочитайте перші `max_bytes` з буфера та виснажіть прочитані байти. Якщо більше запрошено `max_bytes`, Чим доступно в буфері, він витягує стільки байтів, скільки доступно.

### Список параметрів

`max_bytes`

Максимальна кількість байтів для читання із буфера.

### Значення, що повертаються

Повертає прочитаний рядок або **`false`** у разі виникнення помилки.

### список змін

| Версия | Описание |
| --- | --- |
| PECL event 1.6.0 | Перейменований з **EventBuffer::read()** (старе ім'я методу) **EventBuffer::read()**. . **EventBuffer::read()** тепер приймає лише аргумент `max_bytes`; повертає рядок замість цілого числа. |

### Дивіться також

-   [EventBuffer::copyout()](eventbuffer.copyout.md) - Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.md) - Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::pullup()](eventbuffer.pullup.md) - Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
-   [EventBuffer::readLine()](eventbuffer.readline.md) - Витягує рядок із початку буфера
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.md) - Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера