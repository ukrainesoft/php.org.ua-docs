---
navigation:
  - swoole-async.set.md: '« Swoole\\Async::set'
  - swoole-async.writefile.md: 'Swoole\\Async::writeFile »'
  - index.md: PHP Manual
  - class.swoole-async.md: Swoole\\Async
title: 'Swoole\\Async::write'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Async::write

(PECL swoole >= 1.9.0)

Swoole\\Async::write — Асинхронно записує дані у файловий потік

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
