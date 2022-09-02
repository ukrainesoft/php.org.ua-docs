---
navigation:
  - swoole-async.read.md: '« SwooleAsync::read'
  - swoole-async.set.md: 'SwooleAsync::set »'
  - index.md: PHP Manual
  - class.swoole-async.md: SwooleAsync
title: 'SwooleAsync::readFile'
---
# SwooleAsync::readFile

(PECL swoole >= 1.9.0)

SwooleAsync::readFile - Асинхронне читання файлу

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
