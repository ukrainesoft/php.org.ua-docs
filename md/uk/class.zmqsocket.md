---
navigation:
  - zmqcontext.setopt.html: '« ZMQContext::setOpt'
  - zmqsocket.bind.html: 'ZMQSocket::bind »'
  - index.html: PHP Manual
  - book.zmq.html: Обмін повідомленнями 0MQ
title: Клас ZMQSocket
---
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

-   [ZMQSocket::bind](zmqsocket.bind.md) - Прив'язка сокету
-   [ZMQSocket::connect](zmqsocket.connect.md) — Підключення до сокету
-   [ZMQSocket::construct](zmqsocket.construct.md) - Конструктор класу ZMQSocket
-   [ZMQSocket::disconnect](zmqsocket.disconnect.md) - Вимкнути сокет
-   [ZMQSocket::getEndpoints](zmqsocket.getendpoints.md) — Отримати список кінцевих точок
-   [ZMQSocket::getPersistentId](zmqsocket.getpersistentid.md) - Отримати ідентифікатор постійного сокету
-   [ZMQSocket::getSocketType](zmqsocket.getsockettype.md) — Отримати тип сокету
-   [ZMQSocket::getSockOpt](zmqsocket.getsockopt.md) - Отримати опцію сокету
-   [ZMQSocket::isPersistent](zmqsocket.ispersistent.md) — Визначити, чи є сокет постійним
-   [ZMQSocket::recv](zmqsocket.recv.md) - Отримати повідомлення
-   [ZMQSocket::recvMulti](zmqsocket.recvmulti.md) — Отримати повідомлення, яке складається з кількох частин
-   [ZMQSocket::send](zmqsocket.send.md) — Надіслати повідомлення
-   [ZMQSocket::sendmulti](zmqsocket.sendmulti.md) — Надіслати повідомлення, яке складається з кількох частин
-   [ZMQSocket::setSockOpt](zmqsocket.setsockopt.md) - Встановити опцію сокету
-   [ZMQSocket::unbind](zmqsocket.unbind.md) - Відв'язати сокет
