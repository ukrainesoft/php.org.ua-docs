---
navigation:
  - swoole-client.send.md: '« Swoole\\Client::send'
  - swoole-client.sendto.md: 'Swoole\\Client::sendto »'
  - index.md: PHP Manual
  - class.swoole-client.md: Swoole\\Client
title: 'Swoole\\Client::sendfile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Client::sendfile

(PECL swoole >= 1.9.0)

Swoole\\Client::sendfile — Надсилає файл у віддалений TCP-сокет

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
