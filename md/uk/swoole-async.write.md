Асинхронно записує дані у файловий потік

-   [« SwooleAsync::set](swoole-async.set.html)
    
-   [SwooleAsync::writeFile »](swoole-async.writefile.html)
    
-   [PHP Manual](index.md)
    
-   [SwooleAsync](class.swoole-async.html)
    
-   Асинхронно записує дані у файловий потік
    

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