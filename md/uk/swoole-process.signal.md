Надсилає сигнал дочірнім процесам

-   [« SwooleProcess::read](swoole-process.read.html)
    
-   [SwooleProcess::start »](swoole-process.start.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleProcess](class.swoole-process.html)
    
-   Надсилає сигнал дочірнім процесам
    

# SwooleProcess::signal

(PECL swoole >= 1.9.0)

SwooleProcess::signal — Надсилає сигнал дочірнім процесам

### Опис

```methodsynopsis
public static Swoole\Process::signal(string $signal_no, callable $callback): void
```

### Список параметрів

`signal_no`

`callback`

### Значення, що повертаються

У разі успішного відправлення сигналу, повертає TRUE, інакше повертає FALSE.