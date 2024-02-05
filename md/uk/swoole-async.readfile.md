---
navigation:
  - swoole-async.read.md: '« Swoole\\Async::read'
  - swoole-async.set.md: 'Swoole\\Async::set »'
  - index.md: PHP Manual
  - class.swoole-async.md: Swoole\\Async
title: 'Swoole\\Async::readFile'
origin_hash: ddf652f5224dc9f1fa9671347921941ca401ea50
---
# Swoole\\Async::readFile

(PECL swoole >= 1.9.0)

Swoole\\Async::readFile - Асинхронне читання файлу

### Опис

```methodsynopsis
public static Swoole\Async::readFile(string $filename, callable $callback): void
```

### Список параметрів

`filename`

Ім'я файлу, що читається.

`callback`

```methodsynopsis
callback(string $filename, string $content): mixed
```

`filename`

Ім'я файлу, що читається.

`content`

Зміст, прочитаний із файлу.
