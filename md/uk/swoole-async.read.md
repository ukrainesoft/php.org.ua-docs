---
navigation:
  - swoole-async.dnslookup.md: '« Swoole\\Async::dnsLookup'
  - swoole-async.readfile.md: 'Swoole\\Async::readFile »'
  - index.md: PHP Manual
  - class.swoole-async.md: Swoole\\Async
title: 'Swoole\\Async::read'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Async::read

(PECL swoole >= 1.9.0)

Swoole\\Async::read — Асинхронне читання файлового потоку

### Опис

```methodsynopsis
public static Swoole\Async::read(    string $filename,    callable $callback,    int $chunk_size = ?,    int $offset = ?): bool
```

### Список параметрів

`filename`

Назва файлу.

`callback`

```methodsynopsis
callback(string $filename, string $content): mixed
```

`filename`

Назва файлу.

`content`

Вміст, прочитаний із файлового потоку.

`chunk_size`

Довжина частини.

`offset`

Зміщення.

### Значення, що повертаються

Чи успішно прочитано.
