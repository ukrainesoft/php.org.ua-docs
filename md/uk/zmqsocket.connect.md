---
navigation:
  - zmqsocket.bind.md: '« ZMQSocket::bind'
  - zmqsocket.construct.md: 'ZMQSocket::construct »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::connect'
---
# ZMQSocket::connect

(PECL zmq >= 0.5.0)

ZMQSocket::connect — Підключення до сокету

### Опис

```methodsynopsis
public ZMQSocket::connect(string $dsn, bool $force = false): ZMQSocket
```

Підключення сокета до віддаленої кінцевої точки. Кінцева точка вказується у форматі `transport://address`де транспорт може бути одним з наступних значень: inproc, ipc, tcp, pgm або epgm.

### Список параметрів

`dsn`

Ім'я джерела даних, наприклад `transport://address`

`force`

Спробує підключитись навіть якщо сокет вже підключений до зазначеної кінцевої точки.

### Значення, що повертаються

Повертає поточний об'єкт.

### Помилки

Викидає **ZMQSocketException** у разі виникнення помилки.

### Приклади

**Приклад #1 Приклад використання **ZMQContext()****

Створити новий контекст та виділити сокет

```php
<?php
/* Адрес сервера */
$dsn = "tcp://127.0.0.1:5555";

/* Создать сокет */
$socket = new ZMQSocket(new ZMQContext(), ZMQ::SOCKET_REQ, 'my socket');

/* Получить список подключённых конечных точек */
$endpoints = $socket->getEndpoints();

/* Проверить, подключён ли сокет */
if (!in_array($dsn, $endpoints['connect'])) {
    echo "<p>Подключение к $dsn</p>";
    $socket->connect($dsn);
} else {
    echo "<p>Уже подключён к $dsn</p>";
}

/* Послать и получить данные */
$socket->send("Привет!");
$message = $socket->recv();

echo "<p>Сервер ответил: {$message}</p>";
?>
```
