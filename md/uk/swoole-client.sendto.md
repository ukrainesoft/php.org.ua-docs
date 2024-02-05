---
navigation:
  - swoole-client.sendfile.md: '« Swoole\\Client::sendfile'
  - swoole-client.set.md: 'Swoole\\Client::set »'
  - index.md: PHP Manual
  - class.swoole-client.md: Swoole\\Client
title: 'Swoole\\Client::sendto'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Client::sendto

(PECL swoole >= 1.9.0)

Swoole\\Client::sendto — Надсилає дані на віддалену UDP-адресу

### Опис

```methodsynopsis
public Swoole\Client::sendto(string $ip, int $port, string $data): bool
```

Тип клієнта swoole має бути SWOOLE\_SOCK\_UDP або SWOOLE\_SOCK\_UDP6.

### Список параметрів

`ip`

IP-адреса віддаленого хоста, IPv4 або IPv6.

`port`

Номер порту віддаленого хоста.

`data`

Дані для відправки мають бути меншими за 64К.

### Значення, що повертаються
