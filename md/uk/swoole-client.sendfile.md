---
navigation:
  - swoole-client.send.md: '« SwooleClient::send'
  - swoole-client.sendto.md: 'SwooleClient::sendto »'
  - index.md: PHP Manual
  - class.swoole-client.md: SwooleClient
title: 'SwooleClient::sendfile'
---
# SwooleClient::sendfile

(PECL swoole >= 1.9.0)

SwooleClient::sendfile — Надсилає файл у віддалений TCP-сокет

### Опис

```methodsynopsis
public Swoole\Client::sendfile(string $filename, int $offset = ?): bool
```

Є оболонкою системного виклику sendfile в Linux.

### Список параметрів

`filename`

Шлях до файлу для надсилання.

`offset`

Зміщення файлу для надсилання

### Значення, що повертаються
