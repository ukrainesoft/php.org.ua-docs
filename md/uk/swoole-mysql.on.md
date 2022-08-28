Реєструє callback-функцію на основі імені події

-   [« Swoole\\MySQL::getBuffer](swoole-mysql.getbuffer.html)
    
-   [Swoole\\MySQL::query »](swoole-mysql.query.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\MySQL](class.swoole-mysql.html)
    
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