---
navigation:
  - swoole-client.close.md: '« Swoole\\Client::close'
  - swoole-client.construct.md: 'Swoole\\Client::\_\_construct »'
  - index.md: PHP Manual
  - class.swoole-client.md: Swoole\\Client
title: 'Swoole\\Client::connect'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Client::connect

(PECL swoole >= 1.9.0)

Swoole\\Client::connect — Підключається до віддаленого порту TCP або UDP

### Опис

```methodsynopsis
public Swoole\Client::connect(    string $host,    int $port = ?,    int $timeout = ?,    int $flag = ?): bool
```

### Список параметрів

`host`

Ім'я хоста віддаленої адреси.

`port`

Номер порту віддаленої адреси.

`timeout`

Час очікування (у секундах) з'єднання/надсилання/отримання, значення за замовчуванням становить 0,1 с

`flag`

Якщо тип клієнта - UDP, $flag означає, чи ввімкнено конфігурацію udp\_connect. Якщо конфігурація udp\_connect включена, клієнт отримуватиме дані тільки з вказаного ip:port. Якщо тип клієнта TCP, а $flag встановлений на 1, він повинен використовувати swoole\_client\_select для перевірки стану з'єднання перед відправкою/отриманням.

### Значення, що повертаються

Чи встановлено з'єднання.
