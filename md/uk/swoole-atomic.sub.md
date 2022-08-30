Віднімає число із значення атомарного об'єкта

-   [« SwooleAtomic::set](swoole-atomic.set.html)
    
-   [SwooleBuffer »](class.swoole-buffer.html)
    
-   [PHP Manual](index.html)
    
-   [SwooleAtomic](class.swoole-atomic.html)
    
-   Віднімає число із значення атомарного об'єкта
    

# SwooleAtomic::sub

(PECL swoole >= 1.9.0)

SwooleAtomic::sub — Віднімає число із значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::sub(int $sub_value = ?): int
```

Віднімає число із значення атомарного об'єкта.

### Список параметрів

`sub_value`

Значення, яке буде віднято від поточного значення.

### Значення, що повертаються

Поточне значення атомного об'єкта.