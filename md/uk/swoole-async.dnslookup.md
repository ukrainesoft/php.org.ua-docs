---
navigation:
  - class.swoole-async.md: « Swoole\\Async
  - swoole-async.read.md: 'Swoole\\Async::read »'
  - index.md: PHP Manual
  - class.swoole-async.md: Swoole\\Async
title: 'Swoole\\Async::dnsLookup'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Async::dnsLookup

(PECL swoole >= 1.9.0)

Swoole\\Async::dnsLookup — Асинхронний та неблокуючий пошук IP на ім'я хоста

### Опис

```methodsynopsis
public static Swoole\Async::dnsLookup(string $hostname, callable $callback): void
```

**Увага**

Функція поки що не документована; для знайомства доступний лише перелік аргументів.

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
