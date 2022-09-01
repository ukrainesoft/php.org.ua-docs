---
navigation:
  - swoole-client.sendfile.html: '« SwooleClient::sendfile'
  - swoole-client.set.html: 'SwooleClient::set »'
  - index.md: PHP Manual
  - class.swoole-client.html: SwooleClient
title: 'SwooleClient::sendto'
---
# SwooleClient::sendto

(PECL swoole >= 1.9.0)

SwooleClient::sendto — Надсилає дані на віддалену UDP-адресу

### Опис

```methodsynopsis
public Swoole\Client::sendto(string $ip, int $port, string $data): bool
```

Тип клієнта swoole має бути SWOOLESOCKUDP або SWOOLESOCKUDP6.

### Список параметрів

`ip`

IP-адреса віддаленого хоста, IPv4 або IPv6.

`port`

Номер порту віддаленого хоста.

`data`

Дані для відправки мають бути меншими за 64К.

### Значення, що повертаються
