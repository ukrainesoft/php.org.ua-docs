---
navigation:
  - swoole-async.set.html: '« SwooleAsync::set'
  - swoole-async.writefile.html: 'SwooleAsync::writeFile »'
  - index.md: PHP Manual
  - class.swoole-async.html: SwooleAsync
title: 'SwooleAsync::write'
---
# SwooleAsync::write

(PECL swoole >= 1.9.0)

SwooleAsync::write — Асинхронно записує дані у файловий потік

### Опис

```methodsynopsis
public static Swoole\Async::write(    string $filename,    string $content,    int $offset = ?,    callable $callback = ?): void
```

### Список параметрів

`filename`

Назва файлу для запису.

`content`

Зміст для запису файлу.

`offset`

Зміщення.

`callback`
