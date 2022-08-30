Реєструє callback-функцію на основі імені події

-   [« SwooleMySQL::getBuffer](swoole-mysql.getbuffer.html)
    
-   [SwooleMySQL::query »](swoole-mysql.query.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleMySQL](class.swoole-mysql.html)
    
-   Реєструє callback-функцію на основі імені події
    

# SwooleMySQL::on

(PECL swoole >= 1.9.0)

SwooleMySQL::on - Реєструє callback-функцію на основі імені події

### Опис

```methodsynopsis
public Swoole\MySQL::on(string $event_name, callable $callback): void
```

Реєструє callback-функцію на основі імені події, на даний момент підтримується лише подія 'close'.

### Список параметрів

`event_name`

`callback`

### Значення, що повертаються