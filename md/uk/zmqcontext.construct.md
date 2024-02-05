---
navigation:
  - class.zmqcontext.md: « ZMQContext
  - zmqcontext.getopt.md: 'ZMQContext::getOpt »'
  - index.md: PHP Manual
  - class.zmqcontext.md: ZMQContext
title: 'ZMQContext::\_\_construct'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQContext::\_\_construct

(PECL zmq >= 0.5.0)

ZMQContext::\_\_construct - Конструктор ZMQContext

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

Викидає **ZMQContextException**в случае сбоя инициализации контекста.

### Приклади

**Приклад #1 Приклад використання** ZMQContext()\*\*\*\*

Створимо новий контекст та створимо сокети з нього

```php
<?php
/* Создаём новый контекст */
$context = new ZMQContext();

/* Создаём новый сокет */
$socket = $context->getSocket(ZMQ::SOCKET_REQ, 'my sock');

/* Соединяемся с сокетом */
$socket->connect("tcp://example.com:1234");

/* Посылаем запрос */
$socket->send("Hello there");

/* Получаем ответ */
$message = $socket->recv();
?>
```
