---
navigation:
  - eventbuffer.prependbuffer.md: '« EventBuffer::prependBuffer'
  - eventbuffer.read.md: 'EventBuffer::read »'
  - index.md: PHP Manual
  - class.eventbuffer.md: EventBuffer
title: 'EventBuffer::pullup'
---
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

-   [EventBuffer::copyout()](eventbuffer.copyout.md) - Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain()](eventbuffer.drain.md) - Видаляє вказану кількість байтів з початку буфера, нікуди не копіюючи
-   [EventBuffer::read()](eventbuffer.read.md) - Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::readLine()](eventbuffer.readline.md) - Витягує рядок із початку буфера
-   [EventBuffer::appendFrom()](eventbuffer.appendfrom.md) - Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера
