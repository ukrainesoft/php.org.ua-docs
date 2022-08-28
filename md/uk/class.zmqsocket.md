Клас ZMQSocket

-   [« ZMQContext::setOpt](zmqcontext.setopt.html)
    
-   [ZMQSocket::bind »](zmqsocket.bind.html)
    
-   [PHP Manual](index.html)
    
-   [Обмен сообщениями 0MQ](book.zmq.html)
    
-   Клас ZMQSocket
    

# Клас ZMQSocket

(PECL zmq >= 0.5.0)

## Вступ

## Огляд класів

```classsynopsis


    
    
     
      class ZMQSocket
     
     {
    

    /* Методы */
    
   public bind(string $dsn, bool $force = false): ZMQSocket
public connect(string $dsn, bool $force = false): ZMQSocket
public __construct(    ZMQContext $context,    int $type,    string $persistent_id = null,    callable $on_new_socket = null)
public disconnect(string $dsn): ZMQSocket
public getEndpoints(): array
public getPersistentId(): string
public getSocketType(): int
public getSockOpt(string $key): mixed
public isPersistent(): bool
public recv(int $mode = 0): string
public recvMulti(int $mode = 0): array
public send(string $message, int $mode = 0): ZMQSocket
public sendmulti(array $message, int $mode = 0): ZMQSocket
public setSockOpt(int $key, mixed $value): ZMQSocket
public unbind(string $dsn): ZMQSocket

   }
```

## Зміст

-   [ZMQSocket::bind](zmqsocket.bind.html) - Прив'язка сокету
-   [ZMQSocket::connect](zmqsocket.connect.html) — Підключення до сокету
-   [ZMQSocket::\_\_construct](zmqsocket.construct.html) - Конструктор класу ZMQSocket
-   [ZMQSocket::disconnect](zmqsocket.disconnect.html) - Вимкнути сокет
-   [ZMQSocket::getEndpoints](zmqsocket.getendpoints.html) — Отримати список кінцевих точок
-   [ZMQSocket::getPersistentId](zmqsocket.getpersistentid.html) - Отримати ідентифікатор постійного сокету
-   [ZMQSocket::getSocketType](zmqsocket.getsockettype.html) — Отримати тип сокету
-   [ZMQSocket::getSockOpt](zmqsocket.getsockopt.html) - Отримати опцію сокету
-   [ZMQSocket::isPersistent](zmqsocket.ispersistent.html) — Визначити, чи є сокет постійним
-   [ZMQSocket::recv](zmqsocket.recv.html) - Отримати повідомлення
-   [ZMQSocket::recvMulti](zmqsocket.recvmulti.html) — Отримати повідомлення, яке складається з кількох частин
-   [ZMQSocket::send](zmqsocket.send.html) — Надіслати повідомлення
-   [ZMQSocket::sendmulti](zmqsocket.sendmulti.html) — Надіслати повідомлення, яке складається з кількох частин
-   [ZMQSocket::setSockOpt](zmqsocket.setsockopt.html) - Встановити опцію сокету
-   [ZMQSocket::unbind](zmqsocket.unbind.html) - Відв'язати сокет