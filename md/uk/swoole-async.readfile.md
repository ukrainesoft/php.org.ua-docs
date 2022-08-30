Асинхронне читання файлу

-   [« SwooleAsync::read](swoole-async.read.html)
    
-   [SwooleAsync::set »](swoole-async.set.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleAsync](class.swoole-async.html)
    
-   Асинхронне читання файлу
    

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