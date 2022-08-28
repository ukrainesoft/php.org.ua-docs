Асинхронно записує дані у файловий потік

-   [« Swoole\\Async::set](swoole-async.set.html)
    
-   [Swoole\\Async::writeFile »](swoole-async.writefile.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Async](class.swoole-async.html)
    
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