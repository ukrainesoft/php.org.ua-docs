---
navigation:
  - zmqcontext.getopt.md: '« ZMQContext::getOpt'
  - zmqcontext.ispersistent.md: 'ZMQContext::isPersistent »'
  - index.md: PHP Manual
  - class.zmqcontext.md: ZMQContext
title: 'ZMQContext::getSocket'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQContext::getSocket

(PECL zmq >= 0.5.0)

ZMQContext::getSocket — Створює новий сокет

### Опис

```methodsynopsis
public ZMQContext::getSocket(int $type, string $persistent_id = null, callable $on_new_socket = null): ZMQSocket
```

Метод створення сокету з контексту. Якщо контекст не є постійним, то параметр `persistent_id` буде проігноровано та сокет буде непостійним. Функція, задана в `on_new_socket` буде викликана тільки якщо буде створено нову структуру сокету, що лежить в основі.

### Список параметрів

`type`

Константа\*\*`ZMQ::SOCKET_*`\*\*задає тип сокету.

`persistent_id`

Если задан параметр`persistent_id`, то сокет зберігатиметься між запитами.

`on_new_socket`

Callback-функція, яка буде викликана під час створення нової структури сокету. Функція не буде викликана, якщо використовується постійний контекст. Функція приймає як аргументи ZMQSocket і persistent\_id.

### Значення, що повертаються

Повертає об'єкт [ZMQSocket](class.zmqsocket.md)

### Помилки

Викидає **ZMQSocketException**в случае возникновения ошибки.

### Приклади

**Пример #1 Пример использования**ZMQContext()\*\*\*\*

Основи

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
echo "Received message: {$message}\n";
?>
```
