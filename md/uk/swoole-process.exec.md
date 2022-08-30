Виконує системні команди

-   [« SwooleProcess::destruct](swoole-process.destruct.html)
    
-   [SwooleProcess::exit »](swoole-process.exit.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleProcess](class.swoole-process.html)
    
-   Виконує системні команди
    

# SwooleProcess::exec

(PECL swoole >= 1.9.0)

SwooleProcess::exec — Виконує системні команди

### Опис

```methodsynopsis
public Swoole\Process::exec(string $exec_file, string $args): ReturnType
```

Процес буде замінено на системний командний процес, на канал до батьківського процесу буде збережено.

### Список параметрів

`exec_file`

`args`

### Значення, що повертаються