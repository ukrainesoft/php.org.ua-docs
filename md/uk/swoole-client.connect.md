---
navigation:
  - swoole-client.close.md: '« SwooleClient::close'
  - swoole-client.construct.md: 'SwooleClient::construct »'
  - index.md: PHP Manual
  - class.swoole-client.md: SwooleClient
title: 'SwooleClient::connect'
---
# SwooleClient::connect

(PECL swoole >= 1.9.0)

SwooleClient::connect — Підключається до віддаленого порту TCP або UDP

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

Якщо тип клієнта - UDP, $flag означає, чи ввімкнено конфігурацію udpconnect. Якщо конфігурація udpconnect включена, клієнт отримуватиме дані тільки з вказаного ip:port. Якщо тип клієнта TCP, а $flag встановлений на 1, він повинен використовувати swooleclientselect для перевірки стану з'єднання перед відправкою/отриманням.

### Значення, що повертаються

Чи встановлено з'єднання.
