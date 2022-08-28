Додає число до значення атомарного об'єкта

-   [« Swoole\\Atomic](class.swoole-atomic.html)
    
-   [Swoole\\Atomic::cmpset »](swoole-atomic.cmpset.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Atomic](class.swoole-atomic.html)
    
-   Додає число до значення атомарного об'єкта
    

# SwooleAtomic::add

(PECL swoole >= 1.9.0)

SwooleAtomic::add — Додає число значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::add(int $add_value = ?): int
```

Додає число значення атомарного об'єкта.

### Список параметрів

`add_value`

Значення, яке буде додано до поточного значення.

### Значення, що повертаються

Нове значення атомарного об'єкта.