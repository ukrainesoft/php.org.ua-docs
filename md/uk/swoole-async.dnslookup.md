---
navigation:
  - class.swoole-async.html: « SwooleAsync
  - swoole-async.read.html: 'SwooleAsync::read »'
  - index.md: PHP Manual
  - class.swoole-async.html: SwooleAsync
title: 'SwooleAsync::dnsLookup'
---
# SwooleAsync::dnsLookup

(PECL swoole >= 1.9.0)

SwooleAsync::dnsLookup — Асинхронний та неблокуючий пошук IP на ім'я хоста

### Опис

```methodsynopsis
public static Swoole\Async::dnsLookup(string $hostname, callable $callback): void
```

**Увага**

На цей час ця функція ще була документована; для ознайомлення доступний лише перелік аргументів.

### Список параметрів

`hostname`

Ім'я хоста.

`callback`

```methodsynopsis
callback(string $hostname, string $ip): mixed
```

`hostname`

Ім'я хоста.

`IP`

IP-адреса.
