Клас ZMQ

-   [« Требования](zmq.requirements.html)
    
-   [ZMQ::\_\_construct »](zmq.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Обмен сообщениями 0MQ](book.zmq.html)
    
-   Клас ZMQ
    

# Клас ZMQ

(PECL zmq >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class ZMQ
     
     {
    
    /* Константы */
    
     const
     int
      SOCKET_PAIR;

    const
     int
      SOCKET_PUB;

    const
     int
      SOCKET_SUB;

    const
     int
      SOCKET_REQ;

    const
     int
      SOCKET_REP;

    const
     int
      SOCKET_XREQ;

    const
     int
      SOCKET_XREP;

    const
     int
      SOCKET_PUSH;

    const
     int
      SOCKET_PULL;

    const
     int
      SOCKET_ROUTER;

    const
     int
      SOCKET_DEALER;

    const
     int
      SOCKET_XPUB;

    const
     int
      SOCKET_XSUB;

    const
     int
      SOCKET_STREAM;

    const
     int
      SOCKOPT_HWM;

    const
     int
      SOCKOPT_SNDHWM;

    const
     int
      SOCKOPT_RCVHWM;

    const
     int
      SOCKOPT_AFFINITY;

    const
     int
      SOCKOPT_IDENTITY;

    const
     int
      SOCKOPT_SUBSCRIBE;

    const
     int
      SOCKOPT_UNSUBSCRIBE;

    const
     int
      SOCKOPT_RATE;

    const
     int
      SOCKOPT_RECOVERY_IVL;

    const
     int
      SOCKOPT_RECONNECT_IVL;

    const
     int
      SOCKOPT_RECONNECT_IVL_MAX;

    const
     int
      SOCKOPT_MCAST_LOOP;

    const
     int
      SOCKOPT_SNDBUF;

    const
     int
      SOCKOPT_RCVBUF;

    const
     int
      SOCKOPT_RCVMORE;

    const
     int
      SOCKOPT_TYPE;

    const
     int
      SOCKOPT_LINGER;

    const
     int
      SOCKOPT_BACKLOG;

    const
     int
      SOCKOPT_MAXMSGSIZE;

    const
     int
      SOCKOPT_SNDTIMEO;

    const
     int
      SOCKOPT_RCVTIMEO;

    const
     int
      SOCKOPT_IPV4ONLY;

    const
     int
      SOCKOPT_LAST_ENDPOINT;

    const
     int
      SOCKOPT_TCP_KEEPALIVE_IDLE;

    const
     int
      SOCKOPT_TCP_KEEPALIVE_CNT;

    const
     int
      SOCKOPT_TCP_KEEPALIVE_INTVL;

    const
     int
      SOCKOPT_TCP_ACCEPT_FILTER;

    const
     int
      SOCKOPT_TCP_ACCEPT_FILTER;

    const
     int
      SOCKOPT_DELAY_ATTACH_ON_CONNECT;

    const
     int
      SOCKOPT_XPUB_VERBOSE;

    const
     int
      SOCKOPT_ROUTER_RAW;

    const
     int
      SOCKOPT_IPV6;

    const
     int
      CTXOPT_MAX_SOCKETS;

    const
     int
      POLL_IN;

    const
     int
      POLL_OUT;

    const
     int
      MODE_NOBLOCK;

    const
     int
      MODE_DONTWAIT;

    const
     int
      MODE_SNDMORE;

    const
     int
      ERR_INTERNAL;

    const
     int
      ERR_EAGAIN;

    const
     int
      ERR_ENOTSUP;

    const
     int
      ERR_EFSM;

    const
     int
      ERR_ETERM;


    /* Methods */
    
   private __construct()

   }
```

## Обумовлені константи

## Типи констант ZMQ

**`ZMQ::SOCKET_PAIR`**

Ексклюзивний парний шаблон

**`ZMQ::SOCKET_PUB`**

Сокет джерела

**`ZMQ::SOCKET_SUB`**

Сокет передплатника

**`ZMQ::SOCKET_REQ`**

Сокет запиту

**`ZMQ::SOCKET_REP`**

Сокет відповіді

**`ZMQ::SOCKET_XREQ`**

Псевдонім для SOCKETDEALER

**`ZMQ::SOCKET_XREP`**

Псевдонім для SOCKETROUTER

**`ZMQ::SOCKET_PUSH`**

Сокет конвеєра відправки

**`ZMQ::SOCKET_PULL`**

Сокет конвеєра прийому

**`ZMQ::SOCKET_ROUTER`**

Розширений REP-сокет, що маршрутизує відповіді споживачам

**`ZMQ::SOCKET_DEALER`**

Розширений REP-сокет, що здійснює балансування навантаження для всіх пов'язаних пар

**`ZMQ::SOCKET_XPUB`**

Аналогічно SOCKETPUB, за винятком того, що ви можете отримувати передплату як повідомлення. Повідомлення про передплату буде 0 (відписатися) або 1 (підписатися) з наступним вмістом повідомлення

**`ZMQ::SOCKET_XSUB`**

Аналогічно SOCKETSUB, за винятком того, що ви можете надсилати підписку як повідомлення. Дивіться SOCKETXPUB.

**`ZMQ::SOCKET_STREAM`**

Використовується для відсилання та прийому даних TCP від ​​не-ØMQ клієнтів. Доступно, якщо скомпільовано із ZeroMQ 4.x або вище (Значення: int).

**`ZMQ::SOCKOPT_HWM`**

Верхня межа для вхідних та вихідних повідомлень жорстко обмежена максимальною кількістю повідомлень, які ØMQ може пам'ятати для одного клієнта, пов'язаного з відповідним сокетом. Встановлення цієї опції для сокету впливатиме лише на з'єднання, встановлені після встановлення. У ZeroMQ 3.x це обгортка для одночасної установки SNDHWM і RCVHWM. (Значення: int).

**`ZMQ::SOCKOPT_SNDHWM`**

Опція ZMQSNDHWM повинна встановлювати верхню межу вихідних повідомлень на конкретному сокеті. Доступно, якщо зібрано із ZeroMQ 3.x або вище (Значення: int).

**`ZMQ::SOCKOPT_RCVHWM`**

Опція SOCKOPTRCVHWM має встановлювати верхню межу для вхідних повідомлень на конкретному сокеті. Доступно, якщо зібрано із ZeroMQ 3.x або вище (Значення: int).

**`ZMQ::SOCKOPT_AFFINITY`**

Встановити подібність потоку введення/виведення (Значення: int)

**`ZMQ::SOCKOPT_IDENTITY`**

Встановити ідентифікатор сокету (Значення: string)

**`ZMQ::SOCKOPT_SUBSCRIBE`**

Встановити фільтр повідомлень. Коректно для сокету передплатника (Значення: string)

**`ZMQ::SOCKOPT_UNSUBSCRIBE`**

Видалити фільтр повідомлень. Коректно для сокету передплатника (Значення: string)

**`ZMQ::SOCKOPT_RATE`**

Встановити швидкість для сокетів групового розсилання (pgm) (Значення: int >= 0)

**`ZMQ::SOCKOPT_RECOVERY_IVL`**

Встановити інтервал відновлення для сокетів групового розсилання (Значення: int >= 0)

**`ZMQ::SOCKOPT_RECONNECT_IVL`**

Встановити початковий інтервал переєднання (Значення: int >= 0)

**`ZMQ::SOCKOPT_RECONNECT_IVL_MAX`**

Встановити максимальний інтервал переєднання (Значення: int >= 0)

**`ZMQ::SOCKOPT_MCAST_LOOP`**

Контроль закольцювання групової розсилки (Значення: int >= 0)

**`ZMQ::SOCKOPT_SNDBUF`**

Встановити розмір буфера передачі ядра (Значення: int >= 0)

**`ZMQ::SOCKOPT_RCVBUF`**

Встановити розмір буфера прийому ядра (Значення: int >= 0)

**`ZMQ::SOCKOPT_RCVMORE`**

Отримати багатоскладові повідомлення (Значення: int)

**`ZMQ::SOCKOPT_TYPE`**

Отримати тип сокету. Коректно для getSockOpt (Значення: int)

**`ZMQ::SOCKOPT_LINGER`**

Лінійне значення сокету. Визначає, як довго сокет блокує спроби очищення повідомлень після закриття. (Значення: int)

**`ZMQ::SOCKOPT_BACKLOG`**

Опція SOCKOPTBACKLOG встановлює максимальну довжину черги клієнтського з'єднання для зазначеного сокету. Працює лише з транспортом орієнтованим на з'єднання. (Значення: int)

**`ZMQ::SOCKOPT_MAXMSGSIZE`**

Обмежує максимальний розмір вхідного повідомлення. -1 означає, що обмежень немає. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: int)

**`ZMQ::SOCKOPT_SNDTIMEO`**

Встановлює час очікування операції надсилання на сокеті. -1 означає відсутність обмежень. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: int)

**`ZMQ::SOCKOPT_RCVTIMEO`**

Встановлює час очікування операції на сокеті. -1 означає відсутність обмежень. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: int)

**`ZMQ::SOCKOPT_IPV4ONLY`**

Якщо 1, то забороняє IPV6. Доступно, якщо зібрано із ZeroMQ 3.x (Значення: int)

**`ZMQ::SOCKOPT_LAST_ENDPOINT`**

Витягує останнього клієнта, що приєднався. Для використання з Wildcard-портами. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: string)

**`ZMQ::SOCKOPT_TCP_KEEPALIVE_IDLE`**

Час простою для надсилання TCP-keepalive. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: int)

**`ZMQ::SOCKOPT_TCP_KEEPALIVE_CNT`**

Підрахувати час для TCP-keepalive. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: int)

**`ZMQ::SOCKOPT_TCP_KEEPALIVE_INTVL`**

Інтервал для TCP-keepalive. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: int)

**`ZMQ::SOCKOPT_DELAY_ATTACH_ON_CONNECT`**

Надіслати рядок CIDR для звірки з вхідним з'єднанням TCP. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: string)

**`ZMQ::SOCKOPT_TCP_ACCEPT_FILTER`**

Надіслати рядок CIDR для звірки з вхідним з'єднанням TCP. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: string)

**`ZMQ::SOCKOPT_XPUB_VERBOSE`**

Встановити XPUB для отримання повідомлення програми для кожного екземпляра передплатника. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: string)

**`ZMQ::SOCKOPT_ROUTER_RAW`**

Якщо 1, то встановлює ROUTER режим "без обробки". У режимі "без обробки", якщо використовується транспорт tcp://, сокет читатиме і писатиме без використання кадрів ZeroMQ. Доступно, якщо зібрано з ZeroMQ 4.0 та вище (Значення: string)

**`ZMQ::SOCKOPT_IPV6`**

Дозволяє IPV6. Доступно, якщо зібрано з ZeroMQ 4.0 та вище (Значення: string)

**`ZMQ::CTXOPT_MAX_SOCKETS`**

Обмеження сокету на контекст. Доступно, якщо зібрано із ZeroMQ 3.x і вище (Значення: int)

**`ZMQ::POLL_IN`**

Опитати щодо вхідних даних

**`ZMQ::POLL_OUT`**

Опитати щодо вихідних даних

**`ZMQ::MODE_NOBLOCK`**

Неблокуюча робота. Оголошено застарілим, використовуйте ZMQ::MODEDONTWAIT

**`ZMQ::MODE_DONTWAIT`**

Неблокуюча робота

**`ZMQ::MODE_SNDMORE`**

Надіслати багатоскладове повідомлення

**`ZMQ::DEVICE_FORWARDER`**

Пристрій пересилання

**`ZMQ::DEVICE_QUEUE`**

Влаштування черги

**`ZMQ::DEVICE_STREAMER`**

Пристрій потокового мовлення

**`ZMQ::ERR_INTERNAL`**

Внутрішня помилка модуля ZMQ

**`ZMQ::ERR_EAGAIN`**

Має на увазі, що операція блокуватиметься при використанні ZMQ::MODEDONTWAIT

**`ZMQ::ERR_ENOTSUP`**

Операція не підтримується типом сокету

**`ZMQ::ERR_EFSM`**

Операція не буде виконана, оскільки сокет перебуває у некоректному стані

**`ZMQ::ERR_ETERM`**

Контекст було перервано

## Зміст

-   [ZMQ::\_\_construct](zmq.construct.html) - Конструктор ZMQ