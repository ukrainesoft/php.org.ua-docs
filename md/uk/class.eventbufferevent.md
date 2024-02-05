---
navigation:
  - eventbuffer.write.md: '« EventBuffer::write'
  - eventbufferevent.close.md: 'EventBufferEvent::close »'
  - index.md: PHP Manual
  - book.event.md: Event
title: Клас EventBufferEvent
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
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

fd

Числовий файловий дескриптор пов'язаний із буферизованим сокетом. Зазвичай є пов'язаним сокетом. Рівний \*\*`null`\*\*якщо відсутній файловий дескриптор (сокет) пов'язаний з буферизованим подією.

priority

Пріоритет подій, які використовуються для буферизованих подій.

input

Нижчележачий об'єкт вхідного буфера ( [EventBuffer](class.eventbuffer.md)

output

Нижчележачий об'єкт вихідного буфера ( [EventBuffer](class.eventbuffer.md)

## Обумовлені константи

**`EventBufferEvent::READING`**

Подія сталася в момент операції читання з буферевенти. Перевірте інші прапори цієї події.

**`EventBufferEvent::WRITING`**

Подія сталася в момент операції запису в буферевенті. Перевірте інші прапори цієї події.

**`EventBufferEvent::EOF`**

Отримано ознаку кінця файлу для буферизованого події.

**`EventBufferEvent::ERROR`**

Відбулася помилка під час операції з буфером. Детальну інформацію про помилку можна отримати за допомогою методів [EventUtil::getLastSocketErrno()](eventutil.getlastsocketerrno.md)и/или[EventUtil::getLastSocketError()](eventutil.getlastsocketerror.md)

**`EventBufferEvent::TIMEOUT`**

**`EventBufferEvent::CONNECTED`**

Запитане з'єднання з bufferevent встановлено.

**`EventBufferEvent::OPT_CLOSE_ON_FREE`**

Закрити транспорт, що знаходиться нижче, коли об'єкт буферизованої події знищено. Буде закрито сокет, знищено буфер тощо.

**`EventBufferEvent::OPT_THREADSAFE`**

Автоматично розміщувати блокування для bufferevent, що дозволяє безпечно використовувати багатопоточність.

**`EventBufferEvent::OPT_DEFER_CALLBACKS`**

Коли прапор встановлено, bufferevent відкладає всі функції зворотного виклику. Дивіться [» Швидке, переносне, неблокуюче мережне програмування з Libevent та відкладеними функціями зворотного виклику (Deferred callbacks)](http://www.wangafu.net/~nickm/libevent-book/Ref6_bufferevent.md#_deferred_callbacks)

**`EventBufferEvent::OPT_UNLOCK_CALLBACKS`**

За замовчуванням, коли bufferevent налаштований як потокобезпечний, для буферизованого події будуть зберігатися блокування при запуску будь-яких функцій користувача зворотного виклику. Установка цього прапора каже Libevent прибирати блокування під час виклику цих callback-функцій.

**`EventBufferEvent::SSL_OPEN`**

Підтвердження SSL завершено

**`EventBufferEvent::SSL_CONNECTING`**

В даний момент SSL бере участь у встановленні з'єднання як клієнт

**`EventBufferEvent::SSL_ACCEPTING`**

В даний момент SSL бере участь у встановленні з'єднання як сервер

## Зміст

-   [EventBufferEvent::close](eventbufferevent.close.md)— Закриває дескриптор файлу, пов'язаний із поточною подією буфера
-   [EventBufferEvent::connect](eventbufferevent.connect.md)— Підключає файловий дескриптор події буфера до вказаної адреси або сокету UNIX
-   [EventBufferEvent::connectHost](eventbufferevent.connecthost.md)— Підключається на ім'я хоста з можливістю асинхронного дозволу DNS
-   [EventBufferEvent::\_\_construct](eventbufferevent.construct.md)— Створює об'єкт EventBufferEvent
-   [EventBufferEvent::createPair](eventbufferevent.createpair.md)— Створює дві буферні події, пов'язані одна з одною
-   [EventBufferEvent::disable](eventbufferevent.disable.md)— Вимикає читання, запис або те й інше у події буфера
-   [EventBufferEvent::enable](eventbufferevent.enable.md)— Включає читання, запис або те й інше у події буфера
-   [EventBufferEvent::free](eventbufferevent.free.md) \- Звільняє подію буфера
-   [EventBufferEvent::getDnsErrorString](eventbufferevent.getdnserrorstring.md)— Повертає рядок, який описує останню невдалу спробу пошуку DNS
-   [EventBufferEvent::getEnabled](eventbufferevent.getenabled.md)— Повертає бітову маску подій, які активовані для буферної події.
-   [EventBufferEvent::getInput](eventbufferevent.getinput.md)— Повертає базовий вхідний буфер, пов'язаний із поточною буферною подією
-   [EventBufferEvent::getOutput](eventbufferevent.getoutput.md)— Повертає базовий вихідний буфер, пов'язаний із поточною буферною подією
-   [EventBufferEvent::read](eventbufferevent.read.md) \- Читає дані буфера
-   [EventBufferEvent::readBuffer](eventbufferevent.readbuffer.md)— Зливає весь вміст буфера введення та поміщає його у буфер.
-   [EventBufferEvent::setCallbacks](eventbufferevent.setcallbacks.md)— Призначає callback-функції для читання, запису та події (стану)
-   [EventBufferEvent::setPriority](eventbufferevent.setpriority.md) \- Надає пріоритет bufferevent
-   [EventBufferEvent::setTimeouts](eventbufferevent.settimeouts.md)— Встановлює час очікування читання та запису для події буфера
-   [EventBufferEvent::setWatermark](eventbufferevent.setwatermark.md)— Регулює водяні знаки читання та/або запису
-   [EventBufferEvent::sslError](eventbufferevent.sslerror.md)— Повертає останню помилку OpenSSL, повідомлену буферною подією
-   [EventBufferEvent::sslFilter](eventbufferevent.sslfilter.md)— Створює нову подію буфера SSL для надсилання своїх даних через іншу подію буфера
-   [EventBufferEvent::sslGetCipherInfo](eventbufferevent.sslgetcipherinfo.md)— Повертає текстовий опис шифру
-   [EventBufferEvent::sslGetCipherName](eventbufferevent.sslgetciphername.md)— Повертає поточне ім'я шифру з'єднання SSL
-   [EventBufferEvent::sslGetCipherVersion](eventbufferevent.sslgetcipherversion.md)— Повертає версію шифру, який використовується поточним SSL-з'єднанням.
-   [EventBufferEvent::sslGetProtocol](eventbufferevent.sslgetprotocol.md)— Повертає ім'я протоколу, який використовується для поточного з'єднання SSL.
-   [EventBufferEvent::sslRenegotiate](eventbufferevent.sslrenegotiate.md)— Повідомляє буферну подію розпочати перегляд SSL
-   [EventBufferEvent::sslSocket](eventbufferevent.sslsocket.md)— Створює нову буферну подію SSL для надсилання своїх даних через SSL у сокет
-   [EventBufferEvent::write](eventbufferevent.write.md)— Додає дані до буфера виводу буферної події
-   [EventBufferEvent::writeBuffer](eventbufferevent.writebuffer.md)— Додає вміст буфера в буфер виводу буферної події
