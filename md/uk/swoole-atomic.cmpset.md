Порівнює та встановлює значення атомарного об'єкта

-   [« Swoole\\Atomic::add](swoole-atomic.add.html)
    
-   [Swoole\\Atomic::\_\_construct »](swoole-atomic.construct.html)
    
-   [PHP Manual](index.html)
    
-   [Swoole\\Atomic](class.swoole-atomic.html)
    
-   Порівнює та встановлює значення атомарного об'єкта
    

# SwooleAtomic::cmpset

(PECL swoole >= 1.9.0)

SwooleAtomic::cmpset — Порівнює та встановлює значення атомарного об'єкта

### Опис

```methodsynopsis
public Swoole\Atomic::cmpset(int $cmp_value, int $new_value): int
```

### Список параметрів

`cmp_value`

Значення порівняння з поточним значенням атомарного об'єкта.

`new_value`

Значення для атомарного об'єкта, якщо значення cmpvalue збігається із поточним значенням атомарного об'єкта.

### Значення, що повертаються

Нове значення атомарного об'єкта.