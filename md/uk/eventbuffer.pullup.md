Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка

-   [« EventBuffer::prependBuffer](eventbuffer.prependbuffer.html)
    
-   [EventBuffer::read »](eventbuffer.read.html)
    
-   [PHP Manual](index.html)
    
-   [EventBuffer](class.eventbuffer.html)
    
-   Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
    

# EventBuffer::pullup

(PECL event >= 1.2.6-beta)

EventBuffer::pullup — Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка

### Опис

```methodsynopsis
public
   EventBuffer::pullup(
    int
     $size
   ): string
```

"Лінеаризує" перші `size` байти буфера, копіюючи або переміщуючи їх у міру необхідності, щоб гарантувати, що всі вони є суміжними і займають один і той же шматок пам'яті. Якщо розмір негативний, функція лінеаризує весь буфер.

**Увага**

Виклик **EventBuffer::pullup()** з великим розміром може бути досить повільним, оскільки потенційно може знадобитися копіювання всього вмісту буфера.

### Список параметрів

`size`

Кількість байтів має бути безперервним у буфері.

### Значення, що повертаються

Якщо `size` більше, ніж кількість байтів у буфері, функція повертає **`null`**. В іншому випадку повертає рядок **EventBuffer::pullup()**

### Дивіться також

-   [EventBuffer::copyout()](eventbuffer.copyout.html) - Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.html) - Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::read()](eventbuffer.read.html) - Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::readLine()](eventbuffer.readline.html) - Витягує рядок із початку буфера
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.html) - Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера