---
navigation:
  - swoole-client.resume.md: '« Swoole\\Client::resume'
  - swoole-client.sendfile.md: 'Swoole\\Client::sendfile »'
  - index.md: PHP Manual
  - class.swoole-client.md: Swoole\\Client
title: 'Swoole\\Client::send'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Client::send

(PECL swoole >= 1.9.0)

Swoole\\Client::send — Надсилає дані у віддалений TCP-сокет

### Опис

```methodsynopsis
public Swoole\Client::send(string $data, string $flag = ?): int
```

### Список параметрів

`data`

Дані для відправки, які можуть бути рядковими чи двійковими

`flag`

### Значення, що повертаються

Якщо клієнт успішно надіслав дані, він повертає довжину надісланих даних. Або він повертає false та встановлює $swoole\_client->errCode. Для синхронного клієнта немає обмежень на надсилання даних. Для асинхронного клієнта обмеження на надсилання даних - socket\_buffer\_size.
