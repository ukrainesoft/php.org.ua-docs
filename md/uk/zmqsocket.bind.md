---
navigation:
  - class.zmqsocket.md: « ZMQSocket
  - zmqsocket.connect.md: 'ZMQSocket::connect »'
  - index.md: PHP Manual
  - class.zmqsocket.md: ZMQSocket
title: 'ZMQSocket::bind'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# ZMQSocket::bind

(PECL zmq >= 0.5.0)

ZMQSocket::bind — Прив'язка сокету

### Опис

```methodsynopsis
public ZMQSocket::bind(string $dsn, bool $force = false): ZMQSocket
```

Привязка сокета к конечной точке. Конечная точка определяется в формате`transport://address`. Як транспорт можуть використовуватися такі протоколи: inproc, ipc, tcp, pgm або epgm

### Список параметрів

`dsn`

Кінцева точка, наприклад `transport://address`

`force`

Вказує, чи намагатиметься підключитися, якщо підключення до вказаної точки вже було встановлено.

### Значення, що повертаються

Повертає поточний об'єкт. У разі помилки викидає виняток ZMQSocketException.
