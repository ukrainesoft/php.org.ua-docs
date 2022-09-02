---
navigation:
  - swoole-async.dnslookup.md: '« SwooleAsync::dnsLookup'
  - swoole-async.readfile.md: 'SwooleAsync::readFile »'
  - index.md: PHP Manual
  - class.swoole-async.md: SwooleAsync
title: 'SwooleAsync::read'
---
# SwooleAsync::read

(PECL swoole >= 1.9.0)

SwooleAsync::read — Асинхронне читання файлового потоку

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
