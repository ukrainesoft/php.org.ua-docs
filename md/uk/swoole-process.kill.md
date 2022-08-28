Надсилає сигнал дочірньому процесу

-   [« Swoole\\Process::freeQueue](swoole-process.freequeue.html)
    
-   [Swoole\\Process::name »](swoole-process.name.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Process](class.swoole-process.html)
    
-   Надсилає сигнал дочірньому процесу
    

# SwooleProcess::kill

(PECL swoole >= 1.9.0)

SwooleProcess::kill — Надсилає сигнал дочірньому процесу

### Опис

```methodsynopsis
public static Swoole\Process::kill(int $pid, int $signal_no = ?): bool
```

Надсилає сигнал дочірньому процесу.

### Список параметрів

`pid`

Ідентифікатор процесу

`signal_no`

Сигнал до відправлення

### Значення, що повертаються

Повертає **`true`** у разі успішного виконання або **`false`** у разі виникнення помилки.