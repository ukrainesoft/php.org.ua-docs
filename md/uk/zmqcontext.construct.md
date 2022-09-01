---
navigation:
  - class.zmqcontext.html: « ZMQContext
  - zmqcontext.getopt.html: 'ZMQContext::getOpt »'
  - index.html: PHP Manual
  - class.zmqcontext.html: ZMQContext
title: 'ZMQContext::construct'
---
# ZMQContext::construct

(PECL zmq >= 0.5.0)

ZMQContext::construct - Конструктор ZMQContext

### Опис

```methodsynopsis
public ZMQContext::__construct(int $io_threads = 1, bool $is_persistent = true)
```

Створює новий контекст ZMQ. Контекст використовується для ініціалізації сокетів. Для ініціалізації постійних сокетів потрібен постійний контекст.

### Список параметрів

`io_threads`

Число потоків введення/виведення в контексті.

`is_persistent`

Визначає, чи контекст буде постійним. Постійний контекст зберігається протягом багатьох запитів і потрібен для постійних з'єднань.

### Помилки

Викидає **ZMQ Context Exception** у разі збою ініціалізації контексту.

### Приклади

**Приклад #1 Приклад використання **ZMQContext()****

Створимо новий контекст та створимо сокети з нього

```php
<?php
/* Создаём новый контекст */
$context = new ZMQContext();

/* Создаём новый сокет */
$socket = $context->getSocket(ZMQ::SOCKET_REQ, 'my sock');

/* Соединяемся с сокетом */
$socket->connect("tcp://example.com:1234");

/* Посылаем запрос */
$socket->send("Hello there");

/* Получаем ответ */
$message = $socket->recv();
?>
```
