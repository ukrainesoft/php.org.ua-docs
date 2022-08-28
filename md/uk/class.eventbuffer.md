Клас EventBuffer

-   [« EventBase::stop](eventbase.stop.html)
    
-   [EventBuffer::add »](eventbuffer.add.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventBuffer
    

# Клас EventBuffer

(PECL event >= 1.5.0)

## Вступ

**EventBuffer** представляє буфер бібліотеки Libevent - допоміжний функціонал для буферизованого вводу/виводу.

Буфери подій зазвичай корисні організації "буферної" частини буферизованого мережевого вводу/вывода.

## Огляд класів

```classsynopsis

     
    
    
    
     
      class EventBuffer
     
     {
    
    /* Константы */
    
     const
     int
      EOL_ANY = 0;

    const
     int
      EOL_CRLF = 1;

    const
     int
      EOL_CRLF_STRICT = 2;

    const
     int
      EOL_LF = 3;

    const
     int
      PTR_SET = 0;

    const
     int
      PTR_ADD = 1;

    /* Свойства */
    public
     readonly
     int
      $length;

    public
     readonly
     int
      $contiguous_space;

    /* Методы */
    
   public
   add(
    string
     $data
   ): bool
public
   addBuffer(
    EventBuffer
     $buf
   ): bool
public
   appendFrom(
    EventBuffer
     $buf
   , 
    int
     $len
   ): int
public
   __construct()
public
   copyout(
    string
     &$data
   , 
    int
     $max_bytes
   ): int
public
   drain(
    int
     $len
   ): bool
public
   enableLocking(): void
public
   expand(
    int
     $len
   ): bool
public
   freeze(
    bool
     $at_front
   ): bool
public
   lock(): void
public
   prepend(
    string
     $data
   ): bool
public
   prependBuffer(
    EventBuffer
     $buf
   ): bool
public
   pullup(
    int
     $size
   ): string
public
   read(
    int
     $max_bytes
   ): string
public
   read(
    mixed
     $fd
   , 
    int
     $howmuch
   ): int
public
   readLine(
    int
     $eol_style
   ): string
public
   search(
    string
     $what
   , 
    int
     $start
     = -1
   , 
    int
     $end
     = -1
   ): mixed
public
   searchEol(
    int
     $start
     = -1
   , 
    int
     $eol_style
     = 
     EventBuffer::EOL_ANY
    
   ): mixed
public
   substr(
    int
     $start
   , 
    int
     $length
    = ?): string
public
   unfreeze(
    bool
     $at_front
   ): bool
public
   unlock(): bool
public
   write(
    mixed
     $fd
   , 
    int
     $howmuch
    = ?): int

   }
```

## Властивості

length

Кількість байт у буфері подій.

contiguousspace

Кількість байтів, що зберігаються суміжно у передній частині буфера. Байти в буфері можуть розташовуватися в різних шматках пам'яті; Якість повертає кількість байт що знаходяться, в даний момент, в першому шматку.

## Обумовлені константи

**`EventBuffer::EOL_ANY`**

Кінець рядка є будь-якою послідовністю будь-якого числа символів перекладу рядка та повернення каретки. Цей формат не є особливо корисним і існує лише для забезпечення зворотної сумісності.

**`EventBuffer::EOL_CRLF`**

Кінець рядка є послідовністю з необов'язкового повернення каретки та перекладу рядка. (тобто або `"\r\n"` або `"\n"` .) Цей формат корисний при розборі текстових Інтернет-протоколів, оскільки стандарти зазвичай наказують позначати кінець рядка як `"\r\n"`, але багато клієнтів використовують просто `"\n"`

**`EventBuffer::EOL_CRLF_STRICT`**

Кінець рядка є послідовністю із символів повернення каретки та перекладу рядка. (Тобто . `"\r\n"` . ASCII-коди **`0x0D`** **`0x0A`**

**`EventBuffer::EOL_LF`**

Кінець рядка є символом перекладу рядка. (тобто . `"\n"` . ASCII-код **`0x0A`**

**`EventBuffer::PTR_SET`**

Прапор використовується як аргумент методу **EventBuffer::setPosition()**. Якщо прапор встановлений, то вказівник позиції переміщається на абсолютну позицію буфері.

**`EventBuffer::PTR_ADD`**

Те саме, що і **`EventBuffer::PTR_SET`** , за винятком, що прапор вказує методом **EventBuffer::setPosition()** перемістити позицію вперед на вказану кількість байт.

## Зміст

-   [EventBuffer::add](eventbuffer.add.html) — Додає дані до кінця буфера подій
-   [EventBuffer::addBuffer](eventbuffer.addbuffer.html) — Переміщує всі дані з буфера екземпляру EventBuffer
-   [EventBuffer::appendFrom](eventbuffer.appendfrom.html) — Переміщує вказану кількість байтів з вихідного буфера до кінця поточного буфера
-   [EventBuffer::\_\_construct](eventbuffer.construct.html) - Створює об'єкт EventBuffer
-   [EventBuffer::copyout](eventbuffer.copyout.html) — Копіює вказану кількість байтів з початку буфера
-   [EventBuffer::drain](eventbuffer.drain.html) — Видаляє вказану кількість байтів із початку буфера, нікуди не копіюючи
-   [EventBuffer::enableLocking](eventbuffer.enablelocking.html) - Опис
-   [EventBuffer::expand](eventbuffer.expand.html) - Резервує простір у буфері
-   [EventBuffer::freeze](eventbuffer.freeze.html) — Запобігає викликам, які змінюють буфер подій у разі успішного виконання
-   [EventBuffer::lock](eventbuffer.lock.html) — Отримує блокування буфера
-   [EventBuffer::prepend](eventbuffer.prepend.html) — Записує дані на початок буфера
-   [EventBuffer::prependBuffer](eventbuffer.prependbuffer.html) — Переміщує всі дані з вихідного буфера на початок поточного буфера
-   [EventBuffer::pullup](eventbuffer.pullup.html) — Лінеаризує дані в буфері та повертає їх вміст у вигляді рядка
-   [EventBuffer::read](eventbuffer.read.html) — Читає дані з evbuffer та виснажує прочитані байти
-   [EventBuffer::readFrom](eventbuffer.readfrom.html) — Читає дані з файлу до кінця буфера
-   [EventBuffer::readLine](eventbuffer.readline.html) — Витягує рядок із початку буфера
-   [EventBuffer::search](eventbuffer.search.html) - Сканує буфер на наявність рядка
-   [EventBuffer::searchEol](eventbuffer.searcheol.html) - Сканує буфер на наявність кінця рядка
-   [EventBuffer::substr](eventbuffer.substr.html) - Обрізає частину даних буфера
-   [EventBuffer::unfreeze](eventbuffer.unfreeze.html) — Повторно включає дзвінки, які змінюють буфер подій
-   [EventBuffer::unlock](eventbuffer.unlock.html) — Знімає блокування, встановлене EventBuffer::lock
-   [EventBuffer::write](eventbuffer.write.html) — Записує вміст буфера у файл чи сокет