---
navigation:
  - swoole-client.resume.md: '« SwooleClient::resume'
  - swoole-client.sendfile.md: 'SwooleClient::sendfile »'
  - index.md: PHP Manual
  - class.swoole-client.md: SwooleClient
title: 'SwooleClient::send'
---
# SwooleClient::send

(PECL swoole >= 1.9.0)

SwooleClient::send — Надсилає дані у віддалений TCP-сокет

### Опис

```methodsynopsis
public Swoole\Client::send(string $data, string $flag = ?): int
```

### Список параметрів

`data`

Дані для відправки, які можуть бути рядковими чи двійковими

`flag`

### Значення, що повертаються

Якщо клієнт успішно надіслав дані, він повертає довжину надісланих даних. Або він повертає false та встановлює $swooleclient->errCode. Для синхронного клієнта немає обмежень на надсилання даних. Для асинхронного клієнта обмеження на надсилання даних - socketbuffersize.
