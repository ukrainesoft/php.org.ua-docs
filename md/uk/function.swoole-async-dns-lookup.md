---
navigation:
  - ref.swoole-funcs.html: « Функции Swoole
  - function.swoole-async-read.html: swooleasyncread »
  - index.html: PHP Manual
  - ref.swoole-funcs.html: Функции Swoole
title: swooleasyncdnslookup
---
# swooleasyncdnslookup

(PECL swoole >= 1.9.0)

swooleasyncdnslookup — Асинхронний та неблокуючий пошук імені хоста або IP-адреси

### Опис

```methodsynopsis
swoole_async_dns_lookup(string $hostname, callable $callback): bool
```

### Список параметрів

`hostname`

Ім'я хоста.

`callback`

```methodsynopsis
callback(string $hostname, string $ip): mixed
```

`hostname`

Ім'я хоста

`IP`

IP-адреса.

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.
