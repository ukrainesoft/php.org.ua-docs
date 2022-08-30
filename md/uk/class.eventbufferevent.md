Клас EventBufferEvent

-   [« EventBuffer::write](eventbuffer.write.html)
    
-   [EventBufferEvent::close »](eventbufferevent.close.html)
    
-   [PHP Manual](index.html)
    
-   [Event](book.event.html)
    
-   Клас EventBufferEvent
    

# Клас EventBufferEvent

(PECL event >= 1.2.6-beta)

## Вступ

Представляє буферизовану подію Libevent.

Зазвичай додатку потрібно зробити буферизацію певної кількості даних на додаток до того, щоб легко реагувати на події. Коли ми, наприклад, хочемо записувати дані, звичайний алгоритм має такий вигляд:

1.  Вирішуємо, що нам треба записати дані у з'єднання; складаємо дані у буфер
    
2.  Очікуємо, коли з'єднання стане доступним для запису
    
3.  Записуємо стільки даних, скільки можемо
    
4.  Запам'ятовуємо, скільки даних записали і якщо залишилися недозаписані дані, чекаємо, коли з'єднання знову стане доступним для запису.
    

Це шаблон буферизованого вводу/виводу настільки поширений, що Libevent надає вбудований механізм для нього. Буферизована подія складається з транспорту (наприклад сокета), буфера читання та буфера запису. На відміну від стандартних подій, які використовують функцію зворотного виклику, коли транспорт стає доступним для читання або запису, буферизована подія викликає функцію зворотного виклику тоді, коли прочитає або запише достатню кількість даних.

## Огляд класів

```classsynopsis

     
    
    
    
     
      final
      class EventBufferEvent
     
     {
    
    /* Константы */
    
     const
     int
      READING = 1;

    const
     int
      WRITING = 2;

    const
     int
      EOF = 16;

    const
     int
      ERROR = 32;

    const
     int
      TIMEOUT = 64;

    const
     int
      CONNECTED = 128;

    const
     int
      OPT_CLOSE_ON_FREE = 1;

    const
     int
      OPT_THREADSAFE = 2;

    const
     int
      OPT_DEFER_CALLBACKS = 4;

    const
     int
      OPT_UNLOCK_CALLBACKS = 8;

    const
     int
      SSL_OPEN = 0;

    const
     int
      SSL_CONNECTING = 1;

    const
     int
      SSL_ACCEPTING = 2;

    /* Свойства */
    public
     int
      $fd;

    public
     int
      $priority;

    public
     readonly
     EventBuffer
      $input;

    public
     readonly
     EventBuffer
      $output;

    /* Методы */
    
   public
   close(): void
public
   connect(
    string
     $addr
   ): bool
public
   connectHost(    
    EventDnsBase
     $dns_base
   ,    
    string
     $hostname
   ,    
    int
     $port
   ,    
    int
     $family
     = EventUtil::AF_UNSPEC
   ): bool
public
   __construct(    
    EventBase
     $base
   ,    
    mixed
     $socket
     = null
   ,    
    int
     $options
     = 0
   ,    
    callable
     $readcb
     = null
   ,    
    callable
     $writecb
     = null
   ,    
    callable
     $eventcb
     = null
   ,    
    mixed
     $arg
     = null
   )
public
   static
   createPair(
    EventBase
     $base
   , 
    int
     $options
     = 0
   ): array
public
   disable(
    int
     $events
   ): bool
public
   enable(
    int
     $events
   ): bool
public
   free(): void
public
   getDnsErrorString(): string
public
   getEnabled(): int
public
   getInput(): EventBuffer
public
   getOutput(): EventBuffer
public
   read(
    int
     $size
   ): string
public
   readBuffer(
    EventBuffer
     $buf
   ): bool
public
   setCallbacks(    
    callable
     $readcb
   ,    
    callable
     $writecb
   ,    
    callable
     $eventcb
   ,    
    mixed
     $arg
    = ?): void
public
   setPriority(
    int
     $priority
   ): bool
public
   setTimeouts(
    float
     $timeout_read
   , 
    float
     $timeout_write
   ): bool
public
   setWatermark(
    int
     $events
   , 
    int
     $lowmark
   , 
    int
     $highmark
   ): void
public
   sslError(): string
public
   static
   sslFilter(    
    EventBase
     $base
   ,    
    EventBufferEvent
     $underlying
   ,    
    EventSslContext
     $ctx
   ,    
    int
     $state
   ,    
    int
     $options
     = 0
   ): EventBufferEvent
public
   sslGetCipherInfo(): string
public
   sslGetCipherName(): string
public
   sslGetCipherVersion(): string
public
   sslGetProtocol(): string
public
   sslRenegotiate(): void
public
   static
   sslSocket(    
    EventBase
     $base
   ,    
    mixed
     $socket
   ,    
    EventSslContext
     $ctx
   ,    
    int
     $state
   ,    
    int
     $options
    = ?): EventBufferEvent
public
   write(
    string
     $data
   ): bool
public
   writeBuffer(
    EventBuffer
     $buf
   ): bool

   }
```

## Властивості

фд

Числовий файловий дескриптор пов'язаний із буферизованим сокетом. Зазвичай є пов'язаним сокетом. Рівний \*\*`null`\*\*якщо відсутній файловий дескриптор (сокет) пов'язаний з буферизованим подією.

priority

Пріоритет подій, що використовуються для буферизованих подій.

input

Нижчележачий об'єкт вхідного буфера ( [EventBuffer](class.eventbuffer.html)

output

Нижчележачий об'єкт вихідного буфера ( [EventBuffer](class.eventbuffer.html)

## Обумовлені константи

**`EventBufferEvent::READING`**

Подія сталася в момент операції читання з буферевенти. Перевірте інші прапори цієї події.

**`EventBufferEvent::WRITING`**

Подія сталася в момент операції запису в буферевенті. Перевірте інші прапори цієї події.

**`EventBufferEvent::EOF`**

Отримано ознаку кінця файлу для буферизованого події.

**`EventBufferEvent::ERROR`**

Відбулася помилка під час операції з буфером. Детальну інформацію про помилку можна отримати за допомогою методів [EventUtil::getLastSocketErrno()](eventutil.getlastsocketerrno.html) та/або [EventUtil::getLastSocketError()](eventutil.getlastsocketerror.html)

**`EventBufferEvent::TIMEOUT`**

**`EventBufferEvent::CONNECTED`**

Запитане з'єднання з bufferevent встановлено.

**`EventBufferEvent::OPT_CLOSE_ON_FREE`**

Закрити нижчий транспорт, коли об'єкт буферизованої події знищено. Буде закрито сокет, знищено буфер тощо.

**`EventBufferEvent::OPT_THREADSAFE`**

Автоматично розміщувати блокування для bufferevent, що дозволяє безпечно використовувати багатопоточність.

**`EventBufferEvent::OPT_DEFER_CALLBACKS`**

Коли прапор встановлено, bufferevent відкладає всі функції зворотного виклику. Дивіться [» Швидке, переносне, неблокуюче мережне програмування з Libevent та відкладеними функціями зворотного виклику (Deferred callbacks)](http://www.wangafu.net/~nickm/libevent-book/Ref6_bufferevent.html#_deferred_callbacks)

**`EventBufferEvent::OPT_UNLOCK_CALLBACKS`**

За замовчуванням, коли bufferevent налаштований як потокобезпечний, для буферизованого події будуть зберігатися блокування при запуску будь-яких функцій користувача зворотного виклику. Установка цього прапора говорить Libevent прибирати блокування при викликі цих callback-функцій.

**`EventBufferEvent::SSL_OPEN`**

Підтвердження SSL завершено

**`EventBufferEvent::SSL_CONNECTING`**

В даний момент SSL бере участь у встановленні з'єднання як клієнт

**`EventBufferEvent::SSL_ACCEPTING`**

В даний момент SSL бере участь у встановленні з'єднання як сервер

## Зміст

-   [EventBufferEvent::close](eventbufferevent.close.html) — Закриває дескриптор файлу, пов'язаний із поточною подією буфера
-   [EventBufferEvent::connect](eventbufferevent.connect.html) — Підключає файловий дескриптор події буфера до вказаної адреси або сокету UNIX
-   [EventBufferEvent::connectHost](eventbufferevent.connecthost.html) — Підключається на ім'я хоста з можливістю асинхронного дозволу DNS
-   [EventBufferEvent::construct](eventbufferevent.construct.html) — Створює об'єкт EventBufferEvent
-   [EventBufferEvent::createPair](eventbufferevent.createpair.html) — Створює дві буферні події, пов'язані одна з одною
-   [EventBufferEvent::disable](eventbufferevent.disable.html) — Вимикає читання, запис або те й інше у події буфера
-   [EventBufferEvent::enable](eventbufferevent.enable.html) — Включає читання, запис чи те, й інше у події буфера
-   [EventBufferEvent::free](eventbufferevent.free.html) - Звільняє подію буфера
-   [EventBufferEvent::getDnsErrorString](eventbufferevent.getdnserrorstring.html) — Повертає рядок, який описує останню невдалу спробу пошуку DNS
-   [EventBufferEvent::getEnabled](eventbufferevent.getenabled.html) — Повертає бітову маску подій, які активовані для буферної події.
-   [EventBufferEvent::getInput](eventbufferevent.getinput.html) — Повертає базовий вхідний буфер, пов'язаний із поточною буферною подією
-   [EventBufferEvent::getOutput](eventbufferevent.getoutput.html) — Повертає базовий вихідний буфер, пов'язаний із поточною буферною подією
-   [EventBufferEvent::read](eventbufferevent.read.html) - Читає дані буфера
-   [EventBufferEvent::readBuffer](eventbufferevent.readbuffer.html) — Зливає весь вміст буфера введення та поміщає його у буфер.
-   [EventBufferEvent::setCallbacks](eventbufferevent.setcallbacks.html) — Призначає callback-функції для читання, запису та події (стану)
-   [EventBufferEvent::setPriority](eventbufferevent.setpriority.html) - Надає пріоритет bufferevent
-   [EventBufferEvent::setTimeouts](eventbufferevent.settimeouts.html) — Встановлює час очікування читання та запису для події буфера
-   [EventBufferEvent::setWatermark](eventbufferevent.setwatermark.html) — Регулює водяні знаки читання та/або запису
-   [EventBufferEvent::sslError](eventbufferevent.sslerror.html) — Повертає останню помилку OpenSSL, повідомлену буферною подією
-   [EventBufferEvent::sslFilter](eventbufferevent.sslfilter.html) — Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера
-   [EventBufferEvent::sslGetCipherInfo](eventbufferevent.sslgetcipherinfo.html) — Повертає текстовий опис шифру
-   [EventBufferEvent::sslGetCipherName](eventbufferevent.sslgetciphername.html) — Повертає поточне ім'я шифру з'єднання SSL
-   [EventBufferEvent::sslGetCipherVersion](eventbufferevent.sslgetcipherversion.html) — Повертає версію шифру, який використовується поточним SSL-з'єднанням.
-   [EventBufferEvent::sslGetProtocol](eventbufferevent.sslgetprotocol.html) — Повертає ім'я протоколу, який використовується для поточного з'єднання SSL.
-   [EventBufferEvent::sslRenegotiate](eventbufferevent.sslrenegotiate.html) — Повідомляє буферну подію розпочати перегляд SSL
-   [EventBufferEvent::sslSocket](eventbufferevent.sslsocket.html) — Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет
-   [EventBufferEvent::write](eventbufferevent.write.html) — Додає дані до буфера виводу буферної події
-   [EventBufferEvent::writeBuffer](eventbufferevent.writebuffer.html) — Додає вміст буфера в буфер виводу буферної події