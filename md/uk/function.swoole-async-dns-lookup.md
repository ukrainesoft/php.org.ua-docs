---
navigation:
  - ref.swoole-funcs.md: « Функції Swoole
  - function.swoole-async-read.md: swoole\_async\_read »
  - index.md: PHP Manual
  - ref.swoole-funcs.md: Функції Swoole
title: swoole\_async\_dns\_lookup
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# swoole\_async\_dns\_lookup

(PECL swoole >= 1.9.0)

swoole\_async\_dns\_lookup — Асинхронний та неблокуючий пошук імені хоста або IP-адреси

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

Повертає **`true`** у разі успішного виконання або \*\*`false`\*\*в случае возникновения ошибки.
